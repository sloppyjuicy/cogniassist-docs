---
id: settings
title: Settings Editor
sidebar_label: Settings Editor
---

To modify the basic settings of a bot, select **Basic Settings** ![](assets\CA_93.png)under the **Settings** module. It directs you the **Basic Setting** screen as shown below.

![](assets\CA_94.png)

Once your AI bot is built and trained, you can You can configure the below basic settings for the AI bot in the CogniAssist paltform.

## Channels

When your AI bot has developed, you'll be deploying it to a broader user community. You will link your AI bot to the external networks such as your own website, Slack, Twilio, Facebook Messenger and more. Here you can view the full list of supported channels. 

1. SocketIO
2. Whatsapp (twilio)
3. Facebook
4. Telegram
5. Slack
6. Google Hangout	
7. Microsoft Bot Framework

By default, the REST channel is enabled which supports one way communication. Example, one to one conversation with the bot. 

The REST channel will provide you with a REST endpoint which posts messages and sends back the bots messages in response to that request.

#### SocketIO

The SocketIO channel uses websockets and it is real-time. 

![](assets\CA_112.png)

Provide the following details and enable the channel.

| Option           | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| bot_message-evt  | It defines the event name used by CogniAssist while sending messages over socket.io. |
| user_message_evt | It defines the event name used by CogniAssist while receiving messages over socket.io. |

Enter the required details and click the toggle icon ![](assets\CA_107.png)to enable the channel.

#### Whatsapp (twilio)

The Twilio connector can be used to deploy your AI bot that is easily accessible over a text message. To do so, you have to have a whatsapp business profile.

![](assets\CA_113.png)

Provide the following details and enable the channel.

| Option        | Description                                 |
| ------------- | ------------------------------------------- |
| account_sid   | It defines the account security identifier. |
| auth-token    | It defines the authorization token number.  |
| twilio_number | It defines the twilio number.               |

Enter the required details and click the toggle icon ![](assets\CA_107.png)to enable the channel.

#### Facebook

You can deploy your AI bot in the Facebook page. To do so, first you need to set up a facebook page.

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

## Live Agent

Chatbots are not meant to replace humans altogether. Many times chatbot will fail to respond satisfactorily or the user would just want to talk or chat with a human right from the initial conversation. When this occurs, the chatbot will pass the chats to a human agent.

Click the **Live Agent** option from the left side menu of the screen. It displays the following screen.

![](assets\CA_100.png)

**Freshchat**

Based on your business requirements, you can use the live agent third party tools.

Provide the following details and enable the live agent settings.

| Option     | Description                                                  |
| ---------- | ------------------------------------------------------------ |
| api_token  | Enter the api token for the respective third party live agent channel. |
| app_id     | Enter the application ID.                                    |
| channel_id | Enter the channel ID.                                        |

***Note*** - You can get the above details from the **Freshchat** portal.

Once you provide all the required details, click the toggle icon as shown below to enable the settings.

![](assets\cw_027.gif)

## NLU Pipeline

NLU pipeline helps you to classify intent, retrieve responses and extract entities. For example, taking a sentence like "I want to perform a electricity bill payment using credit card" and NLU pipeline classifies this sentence as

1. intent - bill payment
2. entities
   - ​	payment category - electricity
   - ​	payment mode - credit card

Click the **NLU Pipeline** option from the left side menu of the screen. It displays the following screen.

![](assets\CA_101.png)

You can add the required NLU pipeline from the following components.

1. Language Initializers
2. Featurizer
3. Tokenizers
4. Intent Classifiers
5. Entity Extractors
6. External Services
7. spell Correctors

Click the Add icon ![](assets\CA_102.png), to add a component to the pipeline and click the Remove icon![](assets\CA_103.png) to remove it from the pipeline.

## Machine Learning

If the bot is unable to answer the user's query, it offers a  fallback response. To classify the user query confidently, you need set the threshold limit for intents and small talks. 

Click the **Machine Learning** option from the left side menu of the screen. It displays the following screen.

![](assets\CA_104.png)

Drag the pointer to the right side to increase the threshold limit and to the left side to decrease the threshold limit.

![](D:\Cogniassist\cogniassist-docs\docs\assets\cw_028.gif)

***Note*** - If the threshold is very high, then the AI bot will provide a response only if the confidence level is high.

## Deployments

You can add multiple deployments for your AI bot in the **Deployments** section.

Click the **Deployments** option from the left side menu of the screen. It displays the following screen.

![](D:\Cogniassist\cogniassist-docs\docs\assets\CA_105.png)

## Knowledge Repositories

You can search knowledge from the external sources. If the user asks any question to the bot and if the bot couldnt find the answers feom its knowledge base, it will use the external knowlege source to answer the queries.

Click the **Knowledge Repositories** option from the left side menu of the screen. It displays the following screen.

![](assets\CA_106.png)

Provide the following details and enable the knowledge repository.

| Option            | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| URL               | Enter the URL of the external source.                        |
| No of Suggestions | Enter the number of suggestions which should be displayed to the user. |

Click the toggle icon![](assets\CA_107.png)to enable the knowledge repository.

## Protect Confidential Data

If you want to mask the confidential entities or slots, you can configure the settings in this section.

Click the **Protect Confidential Data** option from the left side menu of the screen. It displays the following screen.

![](assets\CA_109.png)

Click the Add icon ![](assets\CA_110.png)to add a new entity or slot as follows.

![](assets\CA_111.png)

Provide the following details and add the data to protect its confidentiality.

| Option      | Description                                         |
| ----------- | --------------------------------------------------- |
| Choose type | Select entity or slot from the list.                |
| enter name  | Enter the entity name or slot name. Example, acc_no |

A sample screen with account number masking is shown below.

![](assets\CA_108.png)

Once you configure all the required settings, click **Save** ![](assets\CA_98.png) to save the changes.