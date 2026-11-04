# What can it do?

This is a program is able to extract ALL possible .dta files from all games and their demos that where made with the LS3D engine, which includes:
- Mafia (2002)
- Hidden & Dangerous 2 (2003)
- Hidden & Dangerous 2: Sabre Squadron (2004)
- Wings of war (2004)
- Chameleon (2005)
- Circus Empire (2006)

These .dta files in the games directory are archives, which include multiple files like textures, models, scripts etc. They are encrypted and most of them are compressed.
This is not the first program which is able to extract these files but what I have seen in the past was not very user friendly in my opinion.
The LS3D unpacker uses GUI elements (windows, buttons etc.) from the windows API, so it is just a matter of a few clicks to extract the requested content.
You also do not need any additional .dll files. It can run in any location you want and you can specify where you want to save the extracted content.
It also does not matter what the file names are. The .dta archives are usually encrypted with different encryption keys, this unpacker can find the keys. If you have an archive that results to the error "Key not found", please notifiy me via the issues tab.


# Usage

It may not look very pretty but it does its job.
You just start the LS3Dunpacker.exe from any locations you want.
Hit the top button "SELECT FILE" and, well, select the archive you want to extract, e.g. "Maps.dta".
You find these .dta files in your main directory, where your game is installed.
Now, after you have confirmed it you should see in the status (above the button) the archive you have loaded.
At this point it was sucessfully mounted and is now ready to extract everything.
If you press "SET DESTIONATION AND EXTRACT" a new window will open, where it asks you about the location you want to extract to. You can select any folder you like. In the same window you can also create a new folder and give it a name.
As soon as you hit "OK" it will start the extraction process.

You should see a progress bar, which gives you an idea of how long the extraction take.
Above the progress bar you see the file it is currently extracting.
Below the progress bar is a cancel button, which does what you expect. It will cancel the extraction and tell you how many files it has already extracted. It will not delete the already extracted files, keep that in mind.
Also keep in mind that the program will overwrite files, which have the same names already, without asking you to do so.
This might be important if you extract it in the same folder, where you have modified files you want to keep already.


# Credits

I had to read and learn alot about these archive structures to do this.
I want to thank culticaxe for his help and testing.
I thank FlashX to point me into the right direction by providing me some really helpful information.
A huge help was the following GitHub page, where Mafia files are processed:
https://github.com/MafiaHub/OpenMF-Archived
I have taken some of their functions and modified them to my needs. Some by quiet alot, to make the program more efficient and useful for my needs.
I want to thank HDmaster for his research about the LZSS decompression these files are using. I used his function but changed it to a more C-Style way.

Furthermore I used the following page as reference, the decryption function shown here is identical to what LS3D Unpacker uses:
https://hd2.fandom.com/wiki/DTA
