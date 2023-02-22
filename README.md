# GPT + DALL-E + Whatsapp = AI Assistant 🚀

![Docker](https://github.com/askrella/whatsapp-chatgpt/actions/workflows/docker.yml/badge.svg)
![Prettier](https://github.com/askrella/whatsapp-chatgpt/actions/workflows/prettier.yml/badge.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This WhatsApp bot uses OpenAI's GPT and DALL-E 2 to respond to user inputs.

![image](https://user-images.githubusercontent.com/95544839/220648896-9d3d170d-2e64-4d43-a4e5-46c73c9c3604.png)

## Requirements

-   Node.js (18 or newer)
-   A recent version of npm
-   An OpenAI Account

## Installation

1. Clone this repository
2. Install the required packages by running `npm install`
3. Put your OpenAI API key into the `.env` file
    - Example file: [.env-example](https://github.com/askrella/whatsapp-chatgpt/blob/master/.env-example)
    - You can obtain an API key [here](https://platform.openai.com/account/api-keys)
4. Run the bot using `npm run start`
5. Scan the QR code with WhatsApp (link a device)
6. Now you're ready to go! People can send you messages, and the bot will respond to them

## Docker

Make sure to edit the `docker-compose.yml` file and set your own variables there.

```sh
sudo docker-compose up
```

## Usage

To use the bot, simply send a message with the `!gpt`/`!dalle`/`!config` command followed by your prompt. For example:

### GPT

```
!gpt What is the meaning of life?
```

### DALLE
```
!dalle A frog with a red hat is walking on a bridge.
```

### AI Config
To modify the bot's configuration, you can use the `!config` command. For example:

```
!config <target> <type> <value>

e.g.
!config dalle size 256x256
```

## Disable prefix

You can disable the `!gpt`/`!dalle`/`!config` prefix by setting `PREFIX_ENABLED` to `false` in the `.env` file.<br/>
If you disable the prefix, the bot will not support DALL-E, and only GPT will be used.

## Sending messages to yourself

This bot also supports sending messages to yourself.

To use this feature, simply send a message to your own phone number using the WhatsApp link `https://wa.me/<your_phone_number>`.
This will take you to your own chat window.

After gaining access to your own chat, you can send a message to yourself and the bot will respond.

## Disclaimer

The operations performed by this bot are not free. You will be charged by OpenAI for each request you make.

This bot uses Puppeteer to run a real instance of Whatsapp Web to avoid getting blocked.

NOTE: We can't guarantee you will not be blocked by using this method, although it works.
WhatsApp does not allow bots or unofficial clients on their platform, so this shouldn't be considered totally safe.
