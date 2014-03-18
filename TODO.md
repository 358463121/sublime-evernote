# Commands to be implemented

Always available:

+ New empty note
+ Define a unified restricted format for metadata:
    * in Evernote.tmLanguage
    * in markdown2
    * in sublime_evernote
+ **Open Note** add parameters:
  - `note_guid` to allow shortcut to favourite notes.
    If this is specified, the other parameters are ignored.
  - `by_searching` to show prompt for a search query.
  - `from_notebook` to filter notes by notebook.
  - `with_tags` (list) to filter notes by tag.

When view shows a note:

+ Save/Upload as new note (send+open)
+ Save/Upload Note
- Diff local note with online version (approx on the markdown!)

- Autocomplete tags/notebooks
    + In metadata block (detect scope?)
    + trigger autocomplete when prefix is `tags:` and `notebook:`

- Status messages

# Event Listeners

## On Load

- Parse metadata, set flag to signal this is a note
- If `download_on_load` redownload

## On Save

+ If view is a note and `upload_on_save` save to Evernote

## On query context

+ Just check for a note guid in metadata or in view settings

## On query completions

    def on_query_completions(self, view, prefix, locations):