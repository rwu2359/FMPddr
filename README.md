# FMPddr
AppleScript to automate FileMaker DDR into FMPerception

##Required
    Mac only,
    FileMaker Pro Advanced,
    FMPerception

##Installation
Create a new Automator Service action, with no input, pointing to FileMaker Pro Advanced

Select Applescript from the available actions

Copy and paste the code from this scpt file

Ensure you have a file open in FileMaker, and run to test

Once the action is saved, you can add a keyboard shortcut from system preferences to fire the action directly. For a demo and instructions see this video from [Todd Geist](https://vimeo.com/168720475)

##Testing
You can run the code from the Script Editor. Because the refresh is silent, you can see the result (boolean) of whether the refresh command was issued in the Result window.

##Running
This will output an XML DDR from all current files from FileMaker with all sections included - to the last place you saved a DDR. If you need this to be a new location so you don't mangle an existing one, do that manually first.

Similarly, FMPerception will import the Summary.xml from the directory that was last used. If you need to point somewhere else, then do that manually first.

You can then run the file directly from the Script Editor, be selecting the Service you created from inside FileMaker, or any other method of your choosing.

####version history
    1.2 16_05_31, minor timing tweaks
    1.1 16_05_30, initial release

####acknowledgements
initial improvements incorporated from Todd Geist, https://www.geistinteractive.com/#gi-products-home

####small print
Its Automator, it does things to your system. Automatically. It works here (my office), but you will test it on your machine first won't you?
