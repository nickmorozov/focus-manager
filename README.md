# focus-manager
Simple script to handle OSX Focus getting/setting and running logic on outside focus change. 
Uses Shortcuts - OSX only, but focus is synced to iOS/watchOS by default.
Uses crontab for periodic launch, which means that there's a 1 minute delay before logic runs on exgernal focus change (e.g., on schedule).

### Dependensies

* [https://github.com/kerma/defaultbrowser|defaultbrowser] - changes default browser (OSX asks you to confirm each time)
* [https://brew.sh|Homebrew] - optional, helps with install

### Installation
1 Install defaultbrowser with `brew install defaultbrowser`
1 Import all Shortcuts
1 Setup your focus values and logic in Shortcuts
1 Place the `focus` script into you $PATH e.g., .local/bin (make sure it's executable - `chmod a+x focus`)
1 Edit the script to add your logic, e.g., `killall Safari; open Google-Chrome` (might change this shortcut instead or in addition to)
1 Run `focus` once to create a crontab entry
