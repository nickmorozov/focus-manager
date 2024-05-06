# focus-manager
Simple script to handle OSX Focus getting/setting and running logic on outside focus change. 
Uses Shortcuts. OSX only, but focus is synced to iOS/watchOS by default.

### Installation
#Import both Shortcuts
#Setup your focus inside
#Place the script into you $PATH e.g., .local/bin (make sure it's executable - `chmod a+x focus`)
#Edit the script to add your logic, e.g., `killall Safari; open Google-Chrome`
#Run `focus` once to create a crontab entry
