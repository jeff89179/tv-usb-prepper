# TV USB Prepper

This is a small macOS Automator application that removes the dot-underbar files (._) from whatever folder is dragged to it. 
This is helpful when prepping a USB stick for a TV that will display a folder with images or videos as a slideshow.

Samsung and Sony TVs seem choke on those files and don't skip over them, resulting in an unsightly gap in the slideshow or a request for user input.

This Automator built application works in three steps.

1. Notify the user that it is about to run now that a folder has been dragged on it (it will also notify if double clicked on, but no further action). 
2. Changes the directory to the first argument ("$1") defined - which was the folder you dragged to it. Then runs the following command...
    dot_clean -m .
        This runs the dot_clean program with the -m flag (always delete dot underbar files) in the current directory (.).
3. Runs an AppleScript to display a confirmation message at the end.

