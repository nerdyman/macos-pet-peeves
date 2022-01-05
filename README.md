# macOS pet peeves

## Key

- ✅ Resolved by OS config change
- ☑️ Resolved by third party tool

##  File Management

- Finder doesn't support cut (`cmd+x`) for files
- Finder doesn't have a breadcrumb menu and doesn't have `cmd+l` support like Linux file managers and browsers to change the path
- Save/Open dialogs never remember where you were last
- Save/Open dialog UI is all over the place and difficult to navigate
- Save/Open dialog doesn't support typing or editing the path, you have to use the dropdown or buttons
- Spotlight search isn't as helpful as Gnome
- ☑️ Can't add plugins to Spotlight without disabling SIP
    - Resolved by replacing Spotlight with [Raycast](https://www.raycast.com/)
- Can't show hidden files without also showing exentsions on all files (e.g. now "Safari.app" is shown in Spotlight)

## UX

- Can't zoom scroll with mouse wheel in browsers
    - Only scrolling option zooms the entire screen
- ☑️ Emoji Picker is sloooow and pastes the emoji where your cursor is - I want to copy it to my clipboard
    - [Resolved by Raycast Emoji Search Extension](https://www.raycast.com/FezVrasta/emoji)
- Dismissed notifications still show in the slide out menu

## DX

- Can't set a default terminal emulator - it's always iterm

## Window Management

- No "Always on top" functionality to keep some windows above others
- Workspace auto switches when last window is closed
- Closing a window (`cmd+w`) doesn't automatically focus the next available one - it only does this when an app is killed with `cmd+q`
- Can't install customised window managers to resolve the keyboard & workspace issues without disabling security features
- Some windows have a 1px gap at the top showing the background between the window and the menu
- Cursor doesn't move to the active workspace when you switch to a workspace on another monitor using the keyboard

### Notes

Currently using https://ianyh.com/amethyst/ in "Fullscreen" mode with workspaces to automatically maximize windows instead of tiling

## Keyboard Usage

- Tab navigation for dialogs is disabled by default
- No way to navigate Mission Control windows with the keyboard
- Cursor does not always follow when switching workspace or switching monitor with keyboard (apps like MS Teams block focus switching somehow)
- ☑️ `Delete`, `Home`, and `End` keys on external keyboard don't work
    - Resolved with [Karbiner Elements](https://karabiner-elements.pqrs.org/)
- The UK layout sometimes messes up and switches `|` and `` ` `` but the keyboard manager thinks it's correct
    - Then need to use the terminal to delete the keyboard profiles because there's no way to do it in the UI
- There doesn't seem to be much logic around when a shortcut should be option and when it should be command

## Managing Apps

- App store is mostly useless - doesn't even have basic apps like Google Chrome and Firefox
- No built in package manager
    - Need to use third party package managers or go to individual websites to manually download apps likes it's 1999

## Hardware Support

- ☑️ "Natural" scroll direction sets both mouse *and* trackpad scroll direction which means the mouse scroll is backwards
    - Solved by [LinearMouse](https://github.com/lujjjh/LinearMouse)
- ☑️ No way to disable scroll acceleration on external mice (Logitech G502 Hero in this case)
    - Resolved by `defaults write .GlobalPreferences com.apple.scrollwheel.scaling -1` helps a little but it's still accelerated
    - Resolved by [LinearMouse](https://github.com/lujjjh/LinearMouse) also helps but still not as smooth as Linux
- ☑️ Additional mouse buttons (back and forward) don't work in finder but do everywhere else
    - Resolved by [LinearMouse](https://github.com/lujjjh/LinearMouse)
- Rendering of the UI looks terrible on normal HD devices
    - Colors aren't as vibrant as they are on Linux and Windows
    - Fonts are blurry and font weights vary
    - Some colors e.g. bright red look like a bad quality JPEG
    - There was previously an option to change these settings per display but it has been removed in the latest release
- M1 macbook pro 
    - Only supports one external monitor
    - Only has two thunderbolt ports (and nothing else)
    - Wifi is spotty when moving from one network to another (e.g. going from home to office) - it needs turned off and on again

## Upgrades

- OS upgrade broke or removed some things
    - Needed manually to reinstall xcode
    - Nuked my sudoers file, had to edit it again
