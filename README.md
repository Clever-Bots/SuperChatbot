<p align="center"><a href="https://nodei.co/npm/superchatbot/"><img src="https://nodei.co/npm/superchatbot.png"></a></p>
<p align="center"><img src="https://img.shields.io/npm/v/superchatbot?style=for-the-badge"> <<img src="https://img.shields.io/npm/dt/superchatbot?style=for-the-badge">
  
# SuperChatbot
  
SuperChatBot is a quick way to easily make your own Chat Bot which can reply in multiple languages!

#
### 📂 [NPM](https://npmjs.com/superchatbot)
#

# Example
  
## Javascript
```js
const superchatbot = require('superchatbot');

const client = new superchatbot.Client();

client.chat({message:"Hello, How are you?", name:"SuperChatbot", owner:"SexyOwnerlol", user: Cooluniqueuserid-in-number, language:"a__h_leLanguage"}).then(reply => {
console.log(reply);
});
```

## Discord.js
```js
const { Client } = require("discord.js");
const {
  AbortController
} = require("abortcontroller-polyfill/dist/cjs-ponyfill");
const client = new Client({ intents: 513 });
const superchatbot = require("superchatbot");
const x = new superchatbot.Client();
client.on("messageCreate", async message => {
  // client detects a message 
  if(message.author.bot) return;
  // if the author of the message is a bot ignore the case
  message.content = message.content.replace(/@(everyone)/gi, "everyone").replace(/@(here)/gi, "here")
  if(message.content.includes(`@`)) {
    return message.reply({ content: `**:x: Please Don't Mention anyone while talking to me I wil cry 😭**`, ephemeral: true }); 
  }
  if(!message.content) return message.reply({ content: ":x: I could Only Reply to Text Messages", ephemeral: true });
  x.chat({
    message: message.content,
    name: "Type ur Name Here",
    user: message.author.id,
    language: "en"
  }).then(reply => {
    message.channel.sendTyping();
    message.reply(`${reply}`);
  });
});
client.login("Your Token")
  ```
  
# Supported Languages
**Language Name**|**Language Code**
:-----:|:-----:
Automatic|auto
Afrikaans|af
Irish|ga
Albanian|sq
Italian|it
Arabic|ar
Japanese|ja
Azerbaijani|az
Kannada|kn
Basque|eu
Korean|ko
Bengali|bn
Latin|la
Belarusian|be
Latvian|lv
Bulgarian|bg
Lithuanian|lt
Catalan|ca
Macedonian|mk
Chinese Simplified|zh-CN
Malay|ms
Chinese Traditional|zh-TW
Maltese|mt
Croatian|hr
Norwegian|no
Czech|cs
Persian|fa
Danish|da
Polish|pl
Dutch|nl
Portuguese|pt
English|en
Romanian|ro
Esperanto|eo
Russian|ru
Estonian|et
Serbian|sr
Filipino|tl
Slovak|sk
Finnish|fi
Slovenian|sl
French|fr
Spanish|es
Galician|gl
Swahili|sw
Georgian|ka
Swedish|sv
German|de
Tamil|ta
Greek|el
Telugu|te
Gujarati|gu
Thai|th
Haitian Creole|ht
Turkish|tr
Hebrew|iw
Ukrainian|uk
Hindi|hi
Urdu|ur
Hungarian|hu
Vietnamese|vi
Icelandic|is
Welsh|cy
Indonesian|id
Yiddish|yi
