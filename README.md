# macOS pet peeves

## Key

- ✅ Resolved with OS config change
- 🟠 Kind of resolved
- ☑️ Resolved with third party tool

## Useful Links

- [Open source macOS tools](https://github.com/stars/nerdyman/lists/macos-tools)

##  File Management

- Finder doesn't support cut (`cmd+x`) for files
    - Can use `cmd+option+v` to cut instead but it's annoying that `cmd+x` doesn't work as the shortcut is available
- Finder doesn't have a breadcrumb menu and doesn't have `cmd+l` support like browsers and Linux file managers to change the path
    - Can quickly move directory with `cmd+shift+g` overlay but it doesn't start with the current working directory
- Save/Open dialogs don't remember where you were last
- Save/Open dialog UI is all over the place and difficult to navigate
- Save/Open dialog doesn't support typing or editing the path, you have to use the dropdown or buttons
- Open dialog sometimes take a long time to open (3+s)
- Spotlight search isn't as helpful as Gnome's search
- Can't add plugins to Spotlight without disabling SIP
    - ☑️ Resolved by replacing Spotlight with [Raycast](https://www.raycast.com/)
- Can't show hidden files without also showing exentsions on all files (e.g. now "Safari.app" is shown in Spotlight)
- Most of storage taken up by "System Data" but there's no way to clean it up
    - 🟠 Can nuke `~/Library/{Logs,Caches}` from the command line

## UX

- Can't zoom scroll with mouse wheel in browsers
    - Only scrolling option zooms the entire screen
- Emoji Picker is sloooow and pastes the emoji where your cursor is - I want to copy it to my clipboard
    - ☑️ [Resolved by Raycast Emoji Search Extension](https://www.raycast.com/FezVrasta/emoji)
- Dismissed notifications still show in the slide out menu
    - ✅ Can be disabled per-application in System Preferences -> Notifications and Focus -> App -> Uncheck "Show in Notifications Centre"
- Allowing applications access to specific files, folders and events requires an application reload (e.g. launch a game, get prompt to allow access accessiblity API, must restart the game)

## Window Management

- Need to click twice on to focus a window on another monitor, once to focus the screen, then again to focus the window
- No "Always on top" functionality to keep some windows above others
- Workspace auto switches when last window is closed
    - 🟠 `defaults write -g AppleSpacesSwitchOnActivate -bool false`
      - This seems to break `cmd+tab` app switching to the correct workspace when the workspace is on the same screen
- Closing a window (`cmd+w`) doesn't automatically focus the next available one - it only does this when an app is killed with `cmd+q`
- Can't install customised window managers to resolve the keyboard & workspace issues without disabling security features
- Some windows have a 1px gap at the top showing the background between the window and the menu
- Cursor doesn't move to the active workspace when you switch to a workspace on another monitor using the keyboard
    - 🟠 Cursor moves when AltTab is used
- Windows of the same application are minimized when you minimize a window (e.g. when I minimize chrome on one screen it also does it on the other 💩)
- Window managment isn't good at determining which window to choose when application has multiple windows (e.g. one monitor has chrome with fullscreen video playing and workspace is visible, other monitor has chrome on a different workspace - fullscreen window is chosen which disrupts the fullscreen video. i3 and Gnome are good at figuring this out)
- Fullscreen windows (videos) are moved to a separate workspace while in fullscreen mode - why not leave it in the current workspace?
- Can't switch to workspace on other screen with keyboard (e.g. focused on workspace 1 on screen 1, `ctrl+6` to go to workspace 6 on screen 2 does not focus the window on that screen)
- Some windows are too small and can't be maximised, e.g. System Settings

### Notes

Currently using https://ianyh.com/amethyst/ in "Fullscreen" mode with workspaces to automatically maximize windows instead of tiling

## Keyboard Usage

- PITA to add custom global shortcut to execute a script (mic mute toggle in this case)
    - Automator script only worked if System Preferences app was kept open
    - ☑️ Resolved by using custom execute script with Karabiner Elements
- Tab navigation doesn't work on dialogs/modals
    - ✅ Resolved by enabling in keyboard preferences
- No way to navigate Mission Control windows with the keyboard
    - ☑️ Resolved by [AltTab](https://github.com/lwouis/alt-tab-macos)
- Cursor does not always follow when switching workspace or switching monitor with keyboard (apps like MS Teams block focus switching somehow)
- ☑️ `Delete`, `Home`, and `End` keys on external keyboard don't work
    - Resolved with [Karbiner Elements](https://karabiner-elements.pqrs.org/)
- The UK layout sometimes messes up and switches `|` and `` ` `` but the keyboard manager thinks it's correct
    - Then need to use the terminal to delete the keyboard profiles because there's no way to do it in the UI
- There doesn't seem to be much logic around when a shortcut should be option and when it should be command

## Managing Apps

- App store is mostly useless - doesn't have basic apps like Google Chrome and Firefox
- No built in package manager
    - Need go to individual websites to manually download apps like it's 1999 or use third party package managers
- Cumbersome to launch GUI apps from the command line

## Hardware Support

- "Natural" scroll direction sets both mouse *and* trackpad scroll direction which means the mouse scroll is backwards
    - ☑️ Resolved by [LinearMouse](https://github.com/lujjjh/LinearMouse)
- No way to disable scroll acceleration on external mice (Logitech G502 Hero in this case)
    - ☑️ Resolved by `defaults write .GlobalPreferences com.apple.scrollwheel.scaling -1` helps a little but it's still accelerated
    - ☑️ Resolved by [LinearMouse](https://github.com/lujjjh/LinearMouse) also helps but still not as smooth as Linux
- Additional mouse buttons (back and forward) don't work in finder but do everywhere else
    - ☑️ Resolved by [LinearMouse](https://github.com/lujjjh/LinearMouse)
- Rendering of the UI looks terrible on normal HD devices
    - Colors aren't as vibrant as they are on Linux and Windows
    - Fonts are blurry and font weights vary
    - Some colors e.g. bright red look like a bad quality JPEG
    - There was previously an option to change these settings per display but it has been removed in the latest release
- Rendering of UI is a bit blurry even on 4k displays
    - After upgrade to 13.5.2 text is slightly blurry even on a 4k display

## Virtualisation

- Doesn't natively support containers, everything needs to run in a vm

## Gaming

- Keys like ctrl and mouse thumb buttons aren't picked up by games

## Upgrades

- OS upgrades break or remove things
    - Need to manually to reinstall xcode
    - Nukes sudoers file
