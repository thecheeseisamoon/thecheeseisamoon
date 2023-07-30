
Logo
2bored2wait
A proxy to wait out 2b2t.org's way too long queue. Includes a small webserver a REST-like API for external control

Report Bug | Request Feature

Table of Contents
About The Project
A proxy to wait out 2b2t.org's way too long queue.
Please Note that because of security reasons this tool doesn't auto-update without a plug-in (check out the addons section)! Also 2b2w does not show ETA from 2b2t.
The ETA is calculated based on position in the queue. This results in better ETA most of the time.

Built With
node.js
npm
HTML
Getting Started
To get a local copy up and running follow these simple steps.

Prerequisites
Please obtain all required items

A discord bot (optional) (detailed instructions)
Installation
Video installation
Click the picture or link bellow to watch!
Click Me To Watch! Video removed by owner.

https://youtu.be/3kCKnwuiHak Video removed by owner.

Quick Install (64-bit Systems)
Read the code to ensure I'm not stealing your credentials. I'm not, but you shouldn't take my word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.
Download the executable here
(Optional) Take a look at the Configs!
Manual Install (32-bit systems, and fallback for quick install):
Download and install node.js version 16 or above and git. You need git even if you download the repository as zip because it is to install the dependencies via npm.
Open a terminal then clone this repo then cd into folder:
 git clone https://github.com/themoonisacheese/2bored2wait
 cd 2bored2wait
Run yarn to install the required libraries
Start the program with yarn start.
Docker
Read the code to ensure I'm not stealing your credentials. I'm not, but you shouldn't take my word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.
docker run -d -p 8080:8080 -p 25565:25565 -e NODE_CONFIG='{"username": "account email", "accountType": "mojang or microsoft", "mcPassword": "your password", "BotToken": "your discord bot token"}' 2bored2wait/2bored2wait:latest. The docker image is automatically up to date after each push to this repo. Docker images are available for amd64 and arm64 among other platforms.
Open a browser and navigate to http://localhost:8080
Press the "Start queuing" button. The queue position indicator auto-updates, but sometimes it takes a while to start counting (like 1 min).
Once the queue reaches a low number, connect to the Minecraft server at address localhost.
After you log off, click the "stop queuing" button. This is really important, as you will not actually disconnect from 2b2t until you do that.
If you want to change the configuration or you don't want your credentials in the bash history you will have to mount config/local.json manually.

Configuration
You can change all credentials and whether you want update messages by simply editing the values in local.json or deleting that file.
For the quick install, configs are located:
gnu+linux/macos: $HOME/.config/2bored2wait/
windows: C:\Users\USERNAME\AppData\Roaming\2bored2wait\Config\
How to use
Read the code to ensure I'm not stealing your credentials. I'm not, but you shouldn't take my word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.
Run npm start
It will now ask for your Minecraft email and password (or permission to use saved launcher data instead). If you want update messages then you need to type Y otherwise N. If you are using the discord bot you need to add your token. Then answer Y or N if you want to save your Minecraft credentials. If you answer N you will need to re-enter your Minecraft login information into the console each time you start the program.
Refer to Commands on how to use 2b2w from the console. Otherwise keep on reading for the web interface.
Now open a browser and navigate to http://localhost: your web port here (default 8080).
Press the "Start queuing" button. The queue position indicator auto-updates, but sometimes it takes a while to start counting (like 1 min).
Once the queue reaches a low number, connect to the Minecraft server at address localhost.
After you log off, click the "stop queuing" button. This is really important, as you will not actually disconnect from 2b2t until you do that.
Commands
All commands can be used through discord or simply typed in the console window.

Please note that the time zone for the calculations is based off your computer's time!

Here are some basic commands:

start will start the queue. It takes between 15-30 seconds for the bot to update with the queue position.
start 14:00 will start at 2pm.
play 8:00 will try to calculate the right time to join so you can play at 8:00
update will send an update to the current channel with your position and ETA.
stop will stop the queue.
Type help for a full ist of commands

Roadmap and known issues
See the open issues for a list of proposed features (and known issues).

Starting the queue will revoke your Minecraft token. this means that you will not be able to join normal Minecraft servers until you restart the game
If you connect after the queue is finished or reconnect the proxy will send cached data. Otherwise you would fly in an empty world. However not all data will be resend. You can move out of render distance (I find going through a nether portal works best) and return to fix this issue. Sometimes the client renders a cached chunk with a blank texture.
How to make a bug report
Try updating 2bored2wait, run npm update (if you are using the source code), and update your system.

• Give info in bug reports such as....

Output of npm list (if you are using the source code).
Version of program.
Other error messages.
Make a bug report here. Feel free to ask questions or add feature requests as well.

Addons
Auto-Update Allows you to have auto updates! REMOVED DUE TO 404

Contributing
Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are greatly appreciated.

Fork the Project
Create your Feature Branch (git checkout -b themoonisacheese/2bored2wait)
Commit your Changes (git commit -m 'Add some AmazingFeature')
Push to the Branch (git push origin themoonisacheese/2bored2wait)
Open a Pull Request
License
Distributed under the GPL-3.0 License. See this for more information.

Testing
Run npm test to run test.js
