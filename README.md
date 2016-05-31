# FMPddr
AppleScript to automate FileMaker DDR into FMPerception

##Required
    Mac only,
    FileMaker Pro Advanced,
    FMPerception

##Installation
Create a new Automator Service action, with no input, pointing to FileMaker Pro Advanced

Select Applescript from the available actions

Copy and paste the code from ths scpt file

Ensure you have a file open in FileMaker, and run to test

Once the action is saved, you can add a keyboard shortcut from system preferences to fire the action directly. For a demo and instructions see: [https://vimeo.com/168720475]

##Testing
You can run the code from the Script Editor. Because the refresh is silent, you can see the result (boolean) of whether the refresh command was issued in the Result window.

####version history
    1.2 16_05_31, minor timing tweaks
    1.1 16_05_30, initial release

###acknowledgements
improvements incorporated from Todd Geist, 
