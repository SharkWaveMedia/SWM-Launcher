contact sharkstarsllc@gmail.com with any questions and issues. i'm happy to help any time.

THIS LAUNCHER WILL ONLY WORK WITH GAMES THAT YOU ALREADY HAVE INSTALLED ON YOUR PC! all it does is launch the game when you insert the disk and kill it when you eject the disk.

this launcher runs in the background. you'll find it running under "cmd.exe" in your processes in task manager. 

this launcher reads information from drive A:\ only.

make sure you allow 3 seconds between inserting and removing the disk or the launcher can't detect it.

this launcher will work with non-steam games, but it requires more troubleshooting. steam games are the easiest right now.

i'm working on a program that creates launch disk files. i will upload it as soon as it's done. for now, we do it manually. this is how it's done -

your floppy disk needs to have a file on it called autorun.txt. this is what needs to be on it -

title: enter game title however you want to be able to read it
requires_steam: enter yes or no / "requires_steam=yes" "requires_steam=no"

steam_app_id: just do a web search for this. pop the number in here

exe_name: this is the name of the local .exe file. not required for steam games if you have steam required set to yes and the steam app id entered.

launch_args: this is where you can use options like forcing start and bypassing launchers. especially useful for non-steam games.

related_processes: add the .exe filepath of any process preventing the game from closing when the disk is ejected. here's an example - Apex Legends runs easyanticheat_eos.exe during the splash screen instead of the main executable file (r5apex.exe), so you'll put "easyanticheat_eos.exe" here so the launcher will close apex even if you pull the disk at the splash screen.

if you have issues with a game launching, try putting the exe_name path ""in double quotes""

here's a blank template you can use to make your own launch disks -

title=
requires_steam=
steam_app_id=
exe_name=""
launch_args=""
related_processes=


and here are the working launch files. again, this content must be saved to "A:\autorun.txt" for the launcher to detect it. if you save this to blank disk while the launcher is running, the game will launch automatically after saving. to avoid this, save a blank autorun.txt to the disk, wait 3 seconds, then add the content to the .txt file.

Titanfall 2 -

title=Titanfall 2
requires_steam=yes
steam_app_id=1237970
exe_name=""
launch_args=""
related_processes=Titanfall2.exe



Vampire The Masquerade Bloodhunt -

title=Vampire: The Masquerade - Bloodhunt
requires_steam=yes
steam_app_id=760160
related_processes=tiger-64.exe,TigerRelease.exe,EasyAntiCheat.exe,EasyAntiCheat_EOS.exe,Tiger-Win64-Shipping.exe



Doom Eternal - 

title=DOOM Eternal
requires_steam=yes
steam_app_id=782330
related_processes=DOOMEternalx64vk.exe



Forza Horizon 5 -

title=Forza Horizon 5
requires_steam=yes
steam_app_id=1551360
related_processes=ForzaHorizon5.exe



Castle Crashers - 

title=Castle Crashers
requires_steam=yes
steam_app_id=204360
exe_name=""
launch_args=""
related_processes=castle.exe,CastleCrashers.exe




Ride 4 - (this one has issues closing on eject sometimes)

title=Ride 4
requires_steam=yes
steam_app_id=1259980
exe_name=ride4.exe
launch_args=""
related_processes=ride4-Win64-Shipping.exe,ride4.exe




Cyberpunk 2077 - (was working fine for days, won't launch as of 10 minutes ago. will update once fixed)

the exe_name section will likely end in the following:
					"...\SteamLibrary\steamapps\common\Cyberpunk\REDprelauncher.exe"

title=Cyberpunk 2077
requires_steam=no
exe_name=""PATH TO REDPRELAUNCHER.EXE""
launch_args=--launch-game
related_processes=Cyberpunk2077.exe


