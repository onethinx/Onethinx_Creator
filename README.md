# Onethinx_Creator
This project combines the Visual Code setup for the Onethinx Core Module with the magnificent PSoC Creator Schematic Editor &amp; Design Wide Resources Editor

## Preparation
1. Make sure you have the VS Code IDE & Dependencies Pack setup done:
    - For Windows: [VSCode_OnethinxPack_Windows](https://github.com/onethinx/VSCode_OnethinxPack_Windows)
    - For Linux: [VSCode_OnethinxPack_Linux](https://github.com/onethinx/VSCode_OnethinxPack_Linux)
    - For MacOS: [VSCode_OnethinxPack_MacOS](https://github.com/onethinx/VSCode_OnethinxPack_MacOS)
1. Clone or download the project to your local machine.
## Start coding and debugging :-)
1. Start VS Code
1. Load the project: File >> Open (Folder) >> Select the folder of the project >> OK
1. Navigate to source/OnethinxCore/LoRaWAN_keys.h and fill in your LoRaWAN keys.
1. Click "⚙︎ Build" in the status bar to build the project.
    * if it fails to build, try "Clean Reconfigure" + "Clean Rebuild" from the Cmake extension (left bar).
    * if it still fails, try deleting the contents of the 'build/' folder.
1. Debug the project using the (Cortex-) Debug extension from the left bar.
    * depending on your debug adapter select "CM4 Debug Kitprog" or "CM4 Debug J-Link" and press 'start'.
## Description
The red LED will flash with the rate defined in the PSoC Creator project.
The blue LED will first be on during the join procedure.
If successfully joined, the blue LED will turn off for one second. 
A loop where the char-values of 'Hello World' will be sent every 10s is then entered.
If not joined -this may take a long while-, the blue LED will blink fast forever.
## Note
If you like to migrate from an all-in-one package to a split project (with separate dependencies pack), follow [this guide.](https://github.com/onethinx/VSCode_HelloWorld/blob/master/MigrateFromAllinOne.md)