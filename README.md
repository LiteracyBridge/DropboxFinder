# DropboxFinder
Finds the Dropbox path, from the Dropbox configuration file.

When Dropbox is configured on a system, it creates a configuration file, in ~/dropbox/info.json or
in %APPDATA%\Dropbox\info.json or %LOCALAPPDATA%\Dropbox\info.json (as appropriate). This app
finds that file, and returns the 'path' member of 'business' if it exists, or 'personal', otherwise.

To build:
  mvn clean install

To run:
  java -jar target/dbfinder.jar [-e]
    -e	Escape spaces and parentheses with '\'

  Writes the path to the dropbox directory to stdout.

