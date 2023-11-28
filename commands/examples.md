# Commands
### Some basic command examples to use in your bot

- this is the base for every command:
```javascript
const { SlashCommandBuilder } = require('discord.js');
	data: new SlashCommandBuilder()
		.setName('command_Name')
		.setDescription('Description'),
	async execute(interaction) {
		//what does the command do
	},
}; */
```
- how to add a string option:
```javascript
.addStringOption(option => 
			option.setName('string_name')
			.setDescription('description')
			.setRequired(true)),
```
