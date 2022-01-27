# Enemy Territory Quake Wars

The multiplayer master server was shut down in 2020, but thankfully the dedicated team at [TAW](https://taw.net/) have been working hard to provide ways for people to continue playing. This README goes through the installation instructions for a player and a host so that you can play ETQW with your friends again. This also includes links to useful resources and outlines some fixes to common problems.

For even more up to date instructions go to [TAW's Discord](https://discordapp.com/invite/tX7Buk9)

## As a player

1. Download the Community Installer for ETQW: [qwsetup.iso](http://etqw.taw.net/qw/qwsetup.iso) 7.6 GBs.
2. Extract `qwsetup.iso` to a folder of your choosing (probably named ETQW) as though it were a zip file.
3. You will now see a folder structure like this

    ```txt
    📂ETQW
    ┣ 📜.checksum.md5
    ┣ 📜qwsetup.exe
    ┣ 📜qwsetup-1a.bin
    ┣ 📜qwsetup-1b.bin
    ┣ 📜qwsetup-1c.bin
    ┣ 📜qwsetup-2a.bin
    ┗ 📜qwsetup-2b.bin
    ```

    Run `qwsetup.exe` to install ETQW. Follow the prompts. You will also be required to pick an installation directory for ETQW.

    **Note**: After this installation three shortcuts are placed on your Desktop. You may delete these.
4. To start the game, run `START_****.bat` to respectively load the correct mod the server is being hosted with. This will require you to ask your friend who is hosting the server.
5. If unsure, for now run `START_PRO.bat`. This will run the game. One of the first things you will be asked to do is to "login". Select the `default` profile to proceed to the main menu.
6. Inside the main menu you will notice the `Play Online` tab is greyed out. This is intended behaviour. From the menu you are free to change the options however you feel (sound, video, keybinds etc). You may also notice that `alt+tab` does not work while the game is fullscreen. For now, set the game to be windowed and at the end I will provide a link to a fix.
7. Once you are satisfied with the settings, close the game. Instructions from here on outline how to setup a LAN VPN like LogMeIn Hamachi, but not as annoying as Hamachi. Download [ZeroTier One.msi](https://download.zerotier.com/dist/ZeroTier%20One.msi) and follow the prompts to install. This is your client we will be using to connect to the host's network.
8. Open ZeroTier. This may make an icon appear in your dashboard. You will need to right click on it and select "Open Control Panel" to begin configuring it.
9. With the ZeroTier Control Panel open, you will notice a field to input a network to join. This number will be provided to you by the friend hosting the server. Once he gives you the number, paste it in, and select join network.
10. As a player, this is all you need to do. Wait for your hosting friends thumbs up as they will need to accept you to the network. Once done, you may open the game again.
11. To connect to your friend's server you must open the ETQW's game console with the tilde key `~` and type:

    ```txt
    connect <ip-address>
    ```

    Where `<ip-address>` is the ip address of the server from ZeroTier. Again, this should be provided to you by your friend.
12. Play.

## As a host

Steps as a host require you to perform above, but also perform server hosting and admin related tasks regarding ZeroTier.

1. Ensure steps, 1-8 are completed.
2. Visit [https://www.zerotier.com/#](ZeroTier) and login. You may be required to make an account. OAuth options are available thankfully.
3. When logged in you will be looking at a dashboard. First click, `Create A Network`. A new network will appear in your list. Click on it to configure it. You do not need to change anything, but you may want to change the name of the network. Make note of the `Network ID`. This number you will need to provide to your friends (and yourself) for step 9 above.
4. When you or one of the clients joins the server they will appear under `Members` down below. Check the box next to their name that says `Auth`. Optionally, give them a name so you know which computer is which. It is important here that you know which computer in this list is *your* computer that is hosting the server.
5. Make note of your computer's `Managed IP` (under `Members` still) while your friends are connecting to the network.
6. When done, you may host the ETQW server using `serverlauncher.exe` in the `ETQW` folder.
7. The server launcher allows you to configure the server however you please. If you wish to change the `Game` setting, then each player must run the corresponding `START_****.bat` file to start the game. This can be left as protourney. One setting you should change is to enable the setting `LAN Server`. Once you are happy with the settings, start the server.
8. You and your friends can now continue from step 11 above making sure to use the `Managed IP` of your computer as the `<ip-address>` is `connect` command that you noted down earlier.

## Additional links

For enabling `alt+tab`, `alt+enter`, unlocked framerate and much more, head to [PCGamingWiki: Enemy Territory: Quake Wars](https://www.pcgamingwiki.com/wiki/Enemy_Territory:_Quake_Wars) and follow the corresponding steps.
