---
id: utterances
title: Intent & Utterances
sidebar_label: Intent & Utterances
---


Now you have to train your AI bot using utterances, to get the relevant results for the user’s query. An **Intent** is an action that meets a user's request. **Utterances** are a set of common sentences that are mapped to the respective intents. Enter as many utterances as possible to help your bot understand what the user wants, as the user query will be in several ways. 

Example, these utterances have the same meaning, "What is the transaction status?" and "show the status of the transaction".

Select **Utterances** ![](assets\CA_020png.png)under the **Training** module, it directs you to the **Intents & Utterances** screen.

![](assets\CA_021png.png)

### Add Intents and Utterances

To add or search for an intent or utterance, provide the required details in the below fields.

| Option                       | Description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| Language                     | Select the language from the list. It lists the primary and secondary languages. |
| Intent Type                  | Select the intent type. Example, select **Smalltalk** to add an intent related to small talk. |
| Search for intents/utterance | Enter the intent name or utterance in the **Search for intents/utterance** field. You can add a new intent or select the existing intent. |

You can choose any of the below methods to add an intent and its utterances.

1. Add new intent
2. Use pre-existing Intents and Utterances
3. Import Intents and Utterances by uploading .csv files

**Add new FAQ**

Once you enter a new intent name, click the **Add** icon ![](assets\CA_022png.png), click the **Tick** icon ![](assets\CA_024png.png)and add the new intent. 

![](assets\cw_013.gif)

**Upload CSV file**

Once you enter a new intent name, the **Upload CSV** ![](assets\CA_023png.png)button is visible. You can directly upload the file which has the set of utterances for the respective intents.

### Add Utterances

As developers build their assistant, one of the major critical tasks is to add training data for all intents they plan to cover. To ensure their assistant can handle real world conversations, they need to anticipate different variations in which their users can express the same intent. The more varied training data we add, the hope is that the NLU models become more robust to incoming user messages. We think it will be helpful to have an interactive data augmentation tool which helps a developer in coming up with these variations to augment their training data with these varied paraphrases.

Once you add a new intent, you can retrieve an extensive library of utterances instead of creating on your own or you can add your own custom utterances.

Enter a sentence and click the **Augment Training Data** icon ![](assets\CA_025png.png) to generate paraphrases. You can select the required ones from the list and add it to the utterances as shown below. 

![](assets\cw_014.gif)

### Entity Mapping

You can pick and map custom values from the utterances to the entities. So that, it helps the AI bot to detect the custom values from the user's query.

![](assets\cw_017.gif)

- To map a keyword from utterance to the entity, select the required keyword and click **Add an entity for “”** button. 
- Select the relevant entity from the list.
- It will map the keyword to the relevant entity and help the AI bot to identify similar utterances.