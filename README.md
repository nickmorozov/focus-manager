# focus-manager
Simple script to handle OSX Focus getting/setting and running logic on outside focus change. 

1. Uses Shortcuts - OSX only, but focus is synced to iOS/watchOS by default.
1. Uses crontab for periodic launch, which means that there's a 1 minute delay before logic runs on exgernal focus change (e.g., on schedule).

### Dependensies

* [defaultbrowser](https://github.com/kerma/defaultbrowser) - changes default browser (OSX asks you to confirm each time)
* [Homebrew](https://brew.sh) - _optional_, helps with install
* [Actions](https://apps.apple.com/ca/app/actions/id1586435171) - _optional_, useful Shortcuts actions

### Installation
1. Install defaultbrowser with `brew install defaultbrowser`
1. Import all Shortcuts
1. Setup your focus values and logic in Shortcuts
1. Place (symlink) the `focus` script into you $PATH e.g., .local/bin
  1. This is optional only ever needed to run `focus`- script sets full path in crontab regardless
  1. Make sure it's executable - `chmod a+x focus`
1. Edit the script to add your logic, e.g., `killall Safari; open Google-Chrome` (might change this shortcut instead or in addition to)
1. Run `focus` once to create a crontab entry
    1. ⚠️  Adds `SHELL=($SHELL)` to crontab unless it is set already
