# MinecraftWaveArena
A school project that uses a Discord bot to summon waves of mobs on a Minecraft server. It is a fun way to train your combat skills in Minecraft. The project is also compatible with a Raspberry Pi Sense Hat, which can be used to display your progress.

## How to use the Arena
Using Wave Arena is very simple. Once the project is correctly set up on your machine, you only need to know two main commands:

### !arena start
This command prepares your world for the incoming waves. You will be teleported to the center of the world where the arena is located, your inventory will be cleared, and you will receive your starting loot. You can also use this command to restart the arena.

### !wave start
This command triggers the next wave. It only works if you have already used the first command and there is no current wave in progress.

### !help
If you forget any of these commands, you can type !help and the bot will remind you. You may also find some additional quality-of-life commands listed in the help menu.

## How to set up the project
To set up this project, you will need the following materials:

* Raspberry Pi
* Raspberry Pi Sense Hat (Optional)
* Discord Bot
### Set up the container on the Raspberry Pi
Install Podman on your Raspberry Pi if you do not have it already. You can use other container managers, but you may need to adjust the settings in the compose.yml file.

Download the compose.yml file and place it into a separate directory. While in that directory, run the compose.yml file with podman. The command for this is "podman compose up"

### Set up Node-RED and Discord
Open Node-RED in your browser on port 1881 (enter your Raspberry Pi's IP address followed by :1881). If you want to use the Sense Hat features, you will need to install Node-RED separately on the Raspberry Pi and open it on port 1880.

Download the project's Node-RED file and import it. For every node related to Discord, you will need to add your Discord bot's token and the channel ID of the channel you wish to use. In one of the Minecraft-related nodes, change the username from "DarkMiking" to your own username (or the username of any other player you will be playing with).

###How to set up your Minecraft world
Open Minecraft with your preferred client. Go to "Multiplayer" and connect to the server by entering your Raspberry Pi's IP address. The arena event takes place around coordinates 0, 80, 0. Feel free to build your arena there or import an existing one. Once this is done, you should be ready to go!

