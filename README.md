🔷 Gclone is just another Tool like Autorclone/Folderclone/Fclone to bypass 750GB limit by google

## 📗 Pre-requisites:-
1. [Install Python 3.7+](https://www.python.org/downloads/)（Latest version 3.8.3 recommended）
2. You need Generated SAs (using [Autorclone](https://github.com/xyou365/AutoRclone) or [Folderclone](https://github.com/Spazzlo/folderclone))
3. Open **accounts** Folder (inside Autorclone or Folderclone Folder) and select any one of the json files and rename it as **1.json**
4. Zip the accounts Folder and keep it safe
5. Make a new bot from [Bot Father](https://core.telegram.org/bots#6-botfather) and get the **Bot token**
6. Get your own Telegram ID - using this [bot](https://t.me/userinfobot)

## 📙 Deploy On Heroku:-

1. git clone https://github.com/Zero-The-Kamisama/Gclone-HRK-Bot
2. cd Gclone-HRK-Bot
3. Open config.ini (Its inside telegram_gcloner Folder) - Fill the appropriate values
```
[General]
path_to_gclone =./gclone

telegram_token = telegram bot token
user_ids = Your Telegram ID (multiple separated by commas, first ID is admin)
group_ids = Your Telegram Group ID (If you are not adding the bot to any group - you can leave it blank)

gclone_para_override = Leave it Blank
```
4. After filling appropriate values save it.
5. Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
Login into your heroku account with command:
   ---heroku login
Create a new heroku app:
   ---heroku create appname	
Select This App in your Heroku-cli:
   ---heroku git:remote -a appname
Change Dyno Stack to a Docker Container:
   ---heroku stack:set container
Add Private Credentials and Config Stuff:
   ---git add * -f
Commit new changes:
   ---git commit -m "Added Creds"
Push Code to Heroku:
   ---git push heroku master --force
Restart Worker by these commands:
   ---heroku ps:scale worker=0
   ---heroku ps:scale worker=1


## 📙 Deploy On VPS:-
1. git clone https://github.com/Zero-The-Kamisama/Gclone-HRK-Bot
2. cd Gclone-HRK-Bot
3. sudo snap install docker
4. sudo docker build . -t gclone-bot
5. sudo docker run gclone-bot


## 🍎 Running the Bot

1. After Deploying go to Telegram Bot you created before and Press **Start**
2. Upload the **accounts.zip** (we created before) to the bot.
3. Reply to the message with `/sa`
4. Type /`folders` and set your favourite Folders
5. Send or forward a message with a Google Drive link to the bot to start Copying...

## Credits:
🧠 [wrenfairbank](https://github.com/wrenfairbank) - [Here](https://github.com/wrenfairbank/telegram_gcloner) - Original Author of the Bot

🧠 [Seiko](https://github.com/thegreatestminer) - [Here](https://github.com/thegreatestminer/telegram_gcloner) - Made the English version 

🧠 [Smartass](https://github.com/smartass08) - [Here](https://github.com/smartass08/telegram_gcloner) - Added docker and Heroku support
