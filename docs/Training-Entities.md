---
id: entities
title: Entities
sidebar_label: Entities
---

An entity represents a key term or object that is relevant to your intents, which provides a specific context for an intent. Example, location, date, person, etc. when a user makes a request, the AI bot attempts to match the possible slot values in the utterance with the custom values and synonyms in the entities.

You can add, update and delete entities in this section. You can also create custom entities based on your bot's context. Select **Entities** <img src="assets\CA_027.png" style="zoom:50%;" /> under the **Training** module, it directs you to the **Custom Entities** screen.

![](assets\CA_026.png)

### Add Entity

Enter an entity name and click **Add** as shown below.

![](assets\cw_015.gif)

### Edit Entity

You can define synonyms for a specific entity so that the bot knows that the synonym in the user query and the entity name are basically the same thing.

- Intents help your AI bot to understand what the user wants to do.
- Entities represent the information relevant to the user’s intent. Entities help the bot extract useful information from an utterance relevant to the user’s intent.

### Add Synonyms

Synonyms are different words that represent the same meaning. Adding synonyms can improve the response for frequently asked questions.

To define synonyms for an entity, click the **Edit** icon ![](assets\CA_029.png). 

![](assets\CA_028.png)

You can add synonyms for an entity so that AI bot can recognise the value when identifying the slots. For example, an entity value of **payment method** can have the synonyms: payment or payment type. This helps the AI bot to understand that when the user says payment, it tags it to the entity value **payment method**. Select the **Define Synonyms** check box to define synonyms for a custom entity value. 

![](assets\cw_016.gif)


### Regexp entities

Some entities need to match patterns rather than specific terms. For example, national identification numbers, IDs, license plates, and so on. With regexp entities, you can provide [regular expressions](https://github.com/google/re2/wiki/Syntax) for matching.


#### Compound regular expressions
Each regexp entity corresponds to a single pattern, but you can provide multiple regular expressions if they all represent variations of a single pattern. During agent training, all regular expressions of a single entity are combined with the alternation operator (|) to form one compound regular expression.

For example, if you provide the following regular expressions for a phone number:

- ^[2-9]\d{2}-\d{3}-\d{4}$
- ^(1?(-?\d{3})-?)?(\d{3})(-?\d{4})$

The compound regular expression becomes:

-  ^[2-9]\d{2}-\d{3}-\d{4}$|^(1?(-?\d{3})-?)?(\d{3})(-?\d{4})$

The ordering of regular expressions matters. Each of the regular expressions in the compound regular expression are processed in order. Searching stops once a valid match is found. For example, for an end user expression of "Seattle":

-  Sea|Seattle matches "Sea"
-  Seattle|Sea matches "Seattle"