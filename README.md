# eggs
Eggs for use with the universal discord bot egg resource. 

The following is an egg for the Pterodactyl Panel [https://pterodactyl.io], made for discord bots and supports pretty much every major language used for them. With this download, you will be able to host any number of discord bots on your own installation of Pterodactyl. Supported languages include: NodeJS, Java/JDK, Python, C# and .NET, PHP 7.2, Lua, and more.

Authentication token in order to be able to pull the Docker containers from the repository. Once you receive your token, you can use it by running

“docker login treasury.forbid.fun -u Automaton -p yourauthkey”

2. Head to the admin area of your Pterodactyl Panel by clicking the gear icon on the top right of the panel


3. Navigate to the "Nests" section of the panel 


5. Enter any name you'd like, for this example, I have used the name "Discord Bot" and for Description, put anything you'd like. When done, click "Save"

6. Now, navigate back to the "Nests" section in the panel, as described in Step 3, and from there, click "Import Egg". Afterward, you will see the following prompt: Select the file "egg-universal-discord-bot-xxxx.json", and "Discord Bot" as the Associated Nest. Upon doing so, click Import.

7. When the import finishes, restart your Pterodactyl Daemon with the following command: “systemctl restart wings”

8. Now that you've imported the egg into Pterodactyl, pull the container that corresponds to the language you're using. 

To find it, open up the .json file for your egg and look for the URL that begins with
“treasury.forbid.fun”

Next, run
“docker pull imageurl”

After you do this and it succeeds, create a new server.

1. All done! The Pterodactyl Egg has successfully been imported. Next time you go to create a server, follow the normal creation steps, just set the relevant values in "Nest Configuration" and alter the field called "Startup Command" to match whatever your bot's startup command is.!
