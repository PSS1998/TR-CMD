# TSMB
Telegram Server Manager Bot - Safe &amp; Easy run command in your RaspberryPi, PC or server from every where.

# How to install and use:
1. To begin, you'll need an Access Token. If you already read and followed [Introduction to the API](https://github.com/python-telegram-bot/python-telegram-bot/wiki/Introduction-to-the-API), you can use the one you generated then. If not: To generate an Access Token, you have to talk to @BotFather and follow a few simple steps ([described here](https://core.telegram.org/bots#6-botfather)). You should really read the introduction first, though.
 Source: [Your first bot from python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot)
 
2. First install some dependencies:
  Best way is use Virtualenv:
  ```bash
  virtualenv -p python3 .env
  source .env/bin/activate
  pip install -r requirements.txt
  ```
  Install these package for using htop command:
  #### In debian base:
  ```bash
  apt-get install htop aha
  ```
  #### In RHEL base:
  ```bash
  yum install htop
  git clone https://github.com/theZiz/aha.git
  cd aha
  make
  make install
  ```
 
3. After create your bot and get your Token from botFather, send some text(more than two message) to your bot and use this command to find your chat_id:
  use @userinfobot bot to get your chat_id by sending /start to bot. 
Put your chat_id and Token(in step1) in config.
 
4. Run code:
 ```bash
 python bot.py
 ```
 
5. Send you command:
  send any command you want like:
  ```bash
 ps -aux
 ```
 
## Sample of htop output:
To get a snapshot of htop, send `/htop` command to bot, output will be like this:

![htop output](https://github.com/MParvin/TSMB/blob/master/htop_output.png?raw=true)
 
## Updates:
 * For more security all response will be sent to the Admin.

## Todo:
* Change admin check structure
* Add debug section, for getting more report
* Use error function in all command functions
* Find best way for detecting interactive commands like htop
* Add one function for all interactive commands
