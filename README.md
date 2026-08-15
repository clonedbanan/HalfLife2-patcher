# Half Life 2-patcher
a script to compile Half Life 2 for Apple Silicon and Intel 64 bit

This script will create an Apple Silicon or Intel 6S bit version of Half Life 2 for macOS.

It is adapted from https://github.com/nonoche2/Portal-patcher, which does the same thing for the original Portal

## How to use:

- to the right of this window, click "releases", expand "assets" if necessary and click on "halflife2.Patcher.zip" to download it
- unzip the file if necessary
- Double click halflife2.command. You will have a Gatekeeper alert preventing the script from running, go to system settings > security and privacy, scroll down and click "open anyway".
- There may also be an issue with permissions so using the command "chmod +x ~/Downloads/halflife2.command" will fix it. if you didn't extract it to the downloads you need to change the commands search location

The script will open the terminal, it will make sure you have all the required dependencies, download/update them if necessary, and prompt you for your Steam login so that it can download the older version of Half Life 2

- type your Steam login and hit enter

you will then be prompted for your Steam password (the terminal won't display anything when you type it, that's normal)
- type your Steam password and hit enter

if necessary, you will then be asked for your Steam guard code. Type it and hit enter.

the script will then download the older version of Half Life 2, download the Source Engine, compile the files and create a Mac version of Half Life 2 in the same location as the script. Depending on your machine, the whole operation can take up to about 15 minutes. The terminal will output a bunch of stuff, and if successfull the last thing you'll see will be "--- Build and Processing Cycle Complete! ---".

## Updating the Steam version

If you don't want the game to run as an independant Application Bundle and want to have it work from Steam:

- after following the instructions above, right-click Half Life 2.app and select "display contents"
- navigate to Contents/Resources/, select all the files inside and copy them
- in Steam, select your installed version of Half Life 2 in the library, click the gear icon and select Manage > browse local files, it'll open a Finder window where the Half Life 2 files are installed
- delete everything except hl2.sh
- paste the files you copied

Normally, Steam communicates with games through a dynamic library which isn't included in this port, so if you want to have Steam launch Half Life 2 in a language other than English, we have to set it up ourselves. In Steam, select Half Life 2 in your library, click on the gear icon, select "properties" and in General > Launch options, type this:  
```-language french -audiolanguage french```

replacing with your language instead of french. the tag '-language' is for the UI and '-audiolanguage' is for the dialogues.
Half Life 2 supports these languages for the audio:

russian  
spanish  
french  
german  

and these languages for the UI:

ukrainian  
swedish  
tchinese (for traditional Chinese)
schinese (for simplified Chinese)  
thai.dat  
thai  
turkish  
brazilian  
bulgarian  
czech  
danish  
dutch  
english  
finnish  
french  
german  
greek  
hungarian  
italian  
japanese  
korean  
koreana  
latam (for latin american Spanish)  
norwegian  
polish  
portuguese  
romanian  
russian  
spanish

you can now launch Half Life 2 from Steam

a similar script is available for [Half Life 2](https://github.com/nonoche2/HL2-patcher/tree/main)
