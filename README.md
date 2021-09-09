# FMPddr
AppleScript to automate FileMaker DDR into FMPerception

## Required
    Mac only
    FileMaker Pro 18+
    FMPerception

## Installation
Create a new Automator Service action (Quick Action 10.14+), with no input, pointing to FileMaker Pro. If you have an ealier one for v16, then you will need to create a new one pointed at your latest version. Call it something different but then you can assign it the same shortcut as the action is linked to the executable...

Select Run Applescript (NOT Execute Applescript) from the available actions

Copy and paste the code from this scpt file

Ensure you have a file open in FileMaker, and run to test. You might need to grant Automator permission to run actions in the Security & Privacy pane.

Once the action is saved, you can add a keyboard shortcut from system preferences to fire the action directly. For a demo and instructions see this video from [Todd Geist](https://vimeo.com/168720475). You might need to grant FileMaker permission in the Security & Privacy pane.

## Testing
You can run the code from the Script Editor. Because the refresh is silent, you can see the result (boolean) of whether the refresh command was issued in the Result window.

## Running
This will output an XML DDR from all current files from FileMaker with all sections included - to the last place you saved a DDR. If you need this to be a new location so you don't mangle an existing one, do that manually first.

Similarly, FMPerception will import the Summary.xml from the directory that was last used. If you need to point somewhere else, then do that manually first.

You can then run the file directly from the Script Editor, by selecting the Service you created from inside FileMaker, the shortcut you assigned to it, or any other method of your choosing.

## Additional files
If you download and use the Custom Function Checker, https://docs.fmperception.com/article/549-extending-fmperception there is AppleScript to automate the export from FMperception into the FileMaker analysis file.

The RunCSV will stop and ask where the export.csv file is ( by default in the same folder as the DDR ) and the updateCSV will export the csv file and then switch to FileMaker and run the import script which refreshes the analysis. 

#### version history
    1.8 21_06_30, added new versions for FMP 19, removed reference to Advanced and refactored some dialog automation
    1.7 18_08_02, explicit instruction to use Run Applescript (thanks to Dave Ramsey)
    1.6 18_05_15, amended for change in High Sierra, and changes in FMP17, fixes #2
    1.5 17_06_15, amended XML checkbox for FMP16 and above - fixes #1
    1.4 16_12_19, changed to point to key command to "refresh", rather than menu item index
    1.3 16_06_08, changed window test for running DDR on remote file
    1.2 16_05_31, minor timing tweaks
    1.1 16_05_30, initial release

#### acknowledgements
initial improvements incorporated from Todd Geist, https://www.geistinteractive.com/#gi-products-home

##### small print
Its Automator, it does things to your system. Automatically. It works here (my office), but you will test it on your machine first won't you? My tests were done today with FMP19.3 on Mojave.
