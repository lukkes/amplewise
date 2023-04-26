
## Installation instructions

- Navigate to https://readwise.io/access_token to find your Readwise Access Token;
- Add it to your plugin settings;
- Fill in the tag you want to apply to all Readwise book notes.

For support, join our Discord and tag @Lucian on the #plugin-atelier channel.

## Usage guide

This plugin makes calls to the Readwise servers to collect books and highlights and add them to your notes.

Good to know:

- This plugin will create a "dashboard note" containing a list of all books;
- For each book, the plugin will create one note;
- Do not edit the contents of the Dashboard note or the contents and the title of the individual note books.

The plugin has to be called manually using the note options, as described below. There is no syncing that will be done automatically.

Note that when making requests to Readwise, we are limited to 20 requests per minute, which is why for accounts with larger amounts of data or for initial syncs, the process will take a few minutes.

This plugin creates 2 new note options:
- "Sync all"
- "Sync this book"

### Sync all

- Invoke this action in a new empty note;
- This note will be filled with links to individual book notes;
- Invoke the plugin again to fetch newer highlights for all books, as well as new books added since the last sync.
- Wait for the confirmation message to make sure that the action finished successfully. Do not edit the resulting notes.

### Sync this book

- Invoke this action in a previously synced note;
- Invoking it again will sync newer highlights;
- The action will fail if the note title doesn't match the required format.
- Do not edit the resulting notes.

## Development notes

When making edits to this plugin, make sure you don't exceed Readwise API rate limiting quotas.
