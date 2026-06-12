# MinecraftWaveArena
A school project, that uses a Discord Bot to summon a wave of mobs on a Minecraft Server. It is a fun way to train your combat skills in Minecraft. It also is compatible with a Sense Hat that will be used to show the progress you've made.
## How to use the Arena
The usage of Wave Arena is very simple. When the Project was setup correctly on your PC you just need to know two commands.
### !arena start
"!arena start", this command sets your world up for the incoming waves. You get teleported to the middle of the world where the arena is, your inventory gets cleared and you get the start loot. You can also use this command if you want to restart the Arena. 
### !wave start
"!wave start", this command starts the next wave. It only works when you have already used the first command and when there is currently no wave in progress. 
### !help
If you forget any of these commands you can also type !help and the bot will remind you. You might also find some additional quality of life commands in the !help command.
## How to setup the Project
To setup this project you also need some material.
* Raspberry PI
* Raspberry PI Sense Hat (Optional)
* Discord Bot
### Setup the container on the Raspberry PI
Install podman on your Raspberry PI if you don't have it yet. You can use other container managers if you would like to but then you might have to adjust some things in the compose.yml file.
Download the compose.yml file and put it into a seperate directory. While you are in this directory run compose.yml.
### Setup Node-Red and Discord
Now you need to open Node-Red in the browser on the port 1881(Type your Raspberry's IP followed by :1881. If you want to use the Sense Hat's features you will need to install Node-Red seperately on the Raspberry PI and then open it on the Port 1880.
Now download the Projects Node Red file and import it there. On every node that is related to Discord you will need to add your Discord bot's Token and the channel-id of the channel you want to use for this. On one of the Minecraft related nodes you have to change the username form "DarkMiking" to your own username (or any other player that you will play this with).
### How to setup your Minecraft World
First open your Minecraft with the client of your preference. Then go to Multiplayer and connect to the server by typing your Raspberry's IP. The arena event happens around the coordinates 0,80,0, feel free to build your arena there or import any arena you might wanna use. After this you should be ready to go.
