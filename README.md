# Discord-Bot-Template
### A base to create discord bots using discord.js version 14

<p align="center">
  <img src='https://raw.github.com/voodootikigod/logo.js/master/specific-uses/badge_js-strict.png' width='150' />
  <img src="https://brandlogos.net/wp-content/uploads/2021/11/discord-logo-512x512.png" width="200" /> 
</p>



How to set up:

- clone the repository;
- (windows) open the cmd in the project directory and run ```npm i```, this will install / update the required modules;
- create a ```config.json``` file and insert your bot token and clientId;
  it should look like this:
```json
{
    "token": "Your-Token",
    "clientId": "Your-Client-Id"
}
```
- set up the commands in the [commands directory](commands/examples.md);
- to run the bot, in the terminal, run ```node .``` or better ```nodemon .```
