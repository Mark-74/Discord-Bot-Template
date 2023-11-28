# Commands
### Some basic command examples to use in your bot

- this is the base for every command:
```javascript
const { SlashCommandBuilder } = require('discord.js');

module.exports = {
	data: new SlashCommandBuilder()
		.setName('command_Name')
		.setDescription('Description'),
	async execute(interaction) {
		//what does the command do
	},
};
```
- how to add a string option:
```javascript
.addStringOption(option => 
			option.setName('string_name')
			.setDescription('description'),
```
- to make a string option required to execute the command:
```javascript
.addStringOption(option => 
			option.setName('string_name')
			.setDescription('description')
			.setRequired(true)),
```
- let's say we want our command to respond to our message:
```javascript
async execute(interaction) {
		interaction.reply('Hi!'); //interaction is an object with multiple methods and attributes
	},
```
- final command with a required string option:
```javascript
const { SlashCommandBuilder } = require('discord.js');

module.exports = {
	data: new SlashCommandBuilder()
		.setName('Greet')
		.setDescription('Says hi to someone!'),

		.addStringOption(option => 
					option.setName('Name')
					.setDescription('Who am i saying Hi to?')
					.setRequired(true)),
	async execute(interaction) {
		//interaction is an object with multiple methods and attributes, you can for example obtain the parameters given when the slash command was launched
		let name = interaction.options.getString('Name') //by doing this I'm getting the string parameter identified with 'Name'
		interaction.reply('Hi ' + name + '!'); 
	},
};
