You need the original full game or shareware data to run:
Place game files in the ".openjazz" directory in "home" folder (/usr/local/home/). This folder is created automatically when you first run the game.

Keys are configurable in the menu.

GAME DATA TROUBLESHOOTING:
All files except .PSM files need to be uppercase in order to be recognised.
If any of the data files are not found openjazz will exit with no warning. You can view the logfile to find out which file(s) you need by enabling Output logs in GMenu2X (press start and change output logs to ON).
Run the game then run Logviewer which appears in the system menu. This will tell you which files are still needed.

NETWORK TROUBLESHOOTING:
Network is supported on local networks (192.168.0.*). I have set the default address to "192.168.0.01234567890123456789". This allows you to select any local IP up to 99 which should be enough.
Left and right D pad to move the cursor and right shoulder button to delete in order to select the correct address of the device you are trying to connect to.
I have successfully connected to a windows installation however the windows installation had trouble connecting to the gcw. I'd suggest hosting on a windows/linux computer.
Networking is experimental and can de-sync.

MUSIC TROUBLESHOOTING:
If you want music you will have to rename the musicfiles (*.PSM) from uppercase to lowercase.
A simple bash (linux) script for this is:
(in openjazz directory)
for $i in *.PSM; do mv $i `echo $i | tr [:upper:] [:lower:]`; done
(This command will work from SSH)

ISSUES:
Save and loading of games is unsupported by openjazz.
The shareware version intro appears to run without problems. The CD version I tested has corruption on the intro video. This appears related to openjazz and not the recompilation.
Openjazz is by no means finished. Enemy boss AI is not implemented, water levels are not working perfectly, weapon launcher physics are not perfect and death sprites are not correctly positioned.

Thanks to Zear for helping build and playtest.
David Knight
