id: smalltalk
title: Smalltalk
sidebar_label: Smalltalk

## Entities

Entities are knowledge repositories, which are used to provide more accurate responses for the user's intent. The entities improve the way AI bot finds the possible matches with the slot values in a user's utterance with your custom slot values. It is a keyword which is extracted from a sentence. Example, location, date, person, etc. when a user makes a request, the AI bot attempts to match the possible slot values in the utterance with the custom values and synonyms in the entities.

You can also create custom entities based on your bot's context. Select **Entities** <img src="D:\Cogniassist\cogniassist-docs\docs\assets\CA_027.png" style="zoom:50%;" /> under the **Training** module, it directs you to the **Custom Entities** screen.

![](D:\Cogniassist\cogniassist-docs\docs\assets\CA_026.png)

### Add Entity

Enter an entity name and click **Add** as shown below.

<img src="D:\Cogniassist\cogniassist-docs\docs\assets\cw_015.gif" style="zoom:67%;" />

### Edit Entity

You can define synonyms for a specific entity so that the bot knows that the synonym in the user query and the entity name are basically the same thing.

- Intents helps your AI bot to understand what the user wants to do.
- Entities represent the information relevant to the user’s intent. Entities helps the bot to extract useful information from an utterance relevant to the user’s intent.

### Add Synonyms

Synonyms are different words that represent the same meaning. Adding synonyms can improve the response for frequently asked questions.

To define synonyms for an entity, click the **Edit** icon <img src="D:\Cogniassist\cogniassist-docs\docs\assets\CA_029.png" style="zoom: 67%;" />. 

![](D:\Cogniassist\cogniassist-docs\docs\assets\CA_028.png)

You can add synonyms for an entity so that AI bot can recognise the value when identifying the slots. For example, an entity value of **payment method** can have the synonyms: payment or payment type. This helps the AI bot to understand that when the user says payment, it tags it to the entity value **payment method**. Select the **Define Synonyms** check box to define synonyms for a custom entity value. 

<img src="D:\Cogniassist\cogniassist-docs\docs\assets\cw_016.gif" style="zoom:67%;" />