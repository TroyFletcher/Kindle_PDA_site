# Kindle_PDA_site
Making a Kindle more PDA-like (WIP)

***Ever wish you had a e-paper display you could customize and control that would permanently display something while sipping battery life?***

![alt text](https://raw.githubusercontent.com/TroyFletcher/Kindle_PDA_site/main/20210811_081820.jpg "sample text")

### An always-on display for you to update with minimal battery life usage! Finally something that doesn't need constant charging to display data or take input!

## Features
1. Display text blobs and todo lists with zero battery usage
2. No hacking/jailbreaking required (but considered)
3. Completely offline (you don't want bezos checking your hardware, right?)
4. Stock on-screen touch keyboard for data entry
5. Get your e-paper display to show the data important to you
6. Instructions to disable screensaver (no hacks/jailbreak)
7. Experimental browser supports picture display and canvas creation (couldn't get it to register javascript mouse or touch events yet)

## Quickstart
1. Attach Kindle as mass storage, send it `kindle.html`
2. Unmount kindle, open experimental browser
3. Browse to `file:///mnt/us/kindle.html`
4. Bookmark this file
5. Tap in boxes to get keyboard, tap out to remove keyboard
6. Pinch zoom-out frequently. Any text entry will auto-zoom in

## Disable screensaver, so browser will stay on screen
1. go to kindle home, enter search term: `;debugOn` press enter to search, 
2. Enter search term: `~ds` press enter to search (if it actually tries to search your library for this term, try `~disableScreensaver`)
3. Enter search term: `;debugOff` press enter to search
4. Screensaver will re-activate on reboot (or maybe like `~es` or something? Idunnolol Try it out)

## Caveats!
1. The screen may be turned off and on without losing form entry data, but pressing HOME will close the browser, and lose info
2. This might just be my version (KOA2), but HTML5 localStorage seems to work only temporary file or memory storage. It wipes after th browser is closed! You can currenlty only save and restore in the same session. It's possible there is a way to fix this
3. Without the screensaver, the device is still scanning for touch events, and therefore using more battery life than if the screensaver was on and waiting for a hardware button press. It is likely it will not last weeks in this state

## Potential future featres
1. The browser support file view and various formats, if you go to `file:///mnt/us/` you have a file view, and can render pictures and text files as well as parse HTML files.
