---
id: settings-channels
title: Channels
sidebar_label: Channels
---

When your AI bot has developed, you'll be deploying it to a broader user community. You will link your AI bot to the external networks such as your own website, Slack, Twilio, Facebook Messenger and more. Each channel has its own salient features. Here you can view the full list of supported channels. 

1. SocketIO
2. Whatsapp (twilio)
3. Facebook
4. Telegram
5. Slack
6. Google Hangout	
7. Microsoft Bot Framework

By default, the REST channel is enabled which supports one way of communication. Example, one-to-one conversation with the bot. 

The REST channel will provide you with a REST endpoint which posts messages and sends back the bots messages in response to that request.

#### SocketIO

The SocketIO channel uses web sockets, and it is real-time. 

![](assets\CA_112.png)

Provide the following details and enable the channel.

| Option           | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| bot_message-evt  | It defines the event name used by CogniAssist while sending messages over SocketIO. |
| user_message_evt | It defines the event name used by CogniAssist while receiving messages over SocketIO. |

Enter the required details and click the toggle icon ![](assets\CA_107.png)to enable the channel.

#### Whatsapp (twilio)

The Twilio connector can be used to deploy your AI bot that is easily accessible over a text message. To do so, you have to have a WhatsApp business profile.

![](assets\CA_113.png)

Provide the following details and enable the channel.

| Option        | Description                                 |
| ------------- | ------------------------------------------- |
| account_sid   | It defines the account security identifier. |
| auth-token    | It defines the authorization token number.  |
| twilio_number | It defines the twilio number.               |

Enter the required details and click the toggle icon ![](assets\CA_107.png)to enable the channel.

#### Facebook

You can deploy your AI bot on the Facebook page. To do so, first you need to set up a Facebook page.

![](assets\CA_114.png)

Provide the following details and enable the channel.

| Option            | Description                              |
| ----------------- | ---------------------------------------- |
| verify            | It defines the verification code.        |
| secret            | It defines the secret code.              |
| page-access-token | It defines the page access token number. |

Enter the required details and click the toggle icon ![](assets\CA_107.png)to enable the channel.

#### Telegram

To deploy your AI bot in Telegram, first you need to create a Telegram bot using the Telegram credentials.

![](assets\CA_115.png)

Provide the following details and enable the channel.

| Option       | Description                         |
| ------------ | ----------------------------------- |
| access_token | It defines the access token number. |
| verify       | It defines the verification code.   |
| webhook_url  | It defines the webhook URL.         |

Enter the required details and click the toggle icon ![](assets\CA_107.png)to enable the channel.

#### Slack

To deploy your AI bot in Slack, first you have to create a Slack app.

![](assets\CA_116.png)

Provide the following details and enable the channel.

| Option      | Description                        |
| ----------- | ---------------------------------- |
| slack_token | It defines the slack token number. |

Enter the required detail and click the toggle icon ![](assets\CA_107.png)to enable the channel.

#### Microsoft Bot Framework

To deploy your AI bot in the Microsoft Bot Framework, first you need to create a Microsoft app.

![](assets\CA_118.png)

Provide the following details and enable the channel.

| Option                 | Description                                    |
| ---------------------- | ---------------------------------------------- |
| MICROSOFT_APP_ID       | It defines the Microsoft application ID.       |
| MICROSOFT_APP_PASSWORD | It defines the Microsoft application password. |

Enter the required details and click the toggle icon ![](assets\CA_107.png)to enable the channel.