id: smalltalk
title: Smalltalk
sidebar_label: Smalltalk

## Training

### Intents and Utterances

Now you have to train your AI bot using utterances, to get the relevant results for the user’s query. An **Intent** is an action that meets a user's request. **Utterances** are a set of common sentences that are mapped to the respective intents. Enter as many utterances as possible to help your bot understand what the user wants, as the user query will be in several ways. 

Example, these utterances have the same meaning, "What is the transaction status?" and "show the status of the transaction".

Select **Utterances** <img src="D:\Cogniassist\cogniassist-docs\docs\assets\CA_020png.png" style="zoom:67%;" />under the **Training** module, it directs you to the **Intents & Utterances** screen.

![](assets\CA_021png.png)

### Add Intents and Utterances

To add or search for an intent or utterance, provide the required details in the below fields.

| Option                       | Description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| Language                     | Select the language from the list. It lists the primary and secondary languages. |
| Intent Type                  | Select the intent type. Example, select **Smalltalk** to add an intent related to small talk. |
| Search for intents/utterance | Enter the intent name or utterance in the **Search for intents/utterance** field. You can add a new intent or select the existing intent. |

You can use any of the below methods to add an intent and its utterances.

Once you enter a new intent name, click the **Add** icon <img src="D:\Cogniassist\cogniassist-docs\docs\assets\CA_022png.png" style="zoom:50%;" />, the **Upload CSV** <img src="D:\Cogniassist\cogniassist-docs\docs\assets\CA_023png.png" style="zoom: 67%;" />button is visible. You can directly upload the file which has the set of utterances for the respective intents or click the **Tick** icon <img src="D:\Cogniassist\cogniassist-docs\docs\assets\CA_024png.png" style="zoom: 67%;" />and add the new intent. 

<img src="D:\Cogniassist\cogniassist-docs\docs\assets\cw_013.gif" style="zoom: 80%;" />

### Add Utterances

Once you add a new intent, you can retrieve an extensive library of built-in utterances instead of creating on your own or you can add your own custom utterances.

To retrieve the built-in utterances, click the **Augment Training Data** icon <img src="D:\Cogniassist\cogniassist-docs\docs\assets\CA_025png.png" style="zoom:50%;" />. You can select the required utterances from the list as shown below. 

<img src="D:\Cogniassist\cogniassist-docs\docs\assets\cw_014.gif" style="zoom:67%;" />

### Entity Mapping

You can pick and map custom values from the utterances to the entities. So that, it helps the AI bot to detect the custom values from the user's query.

<img src="D:\Cogniassist\cogniassist-docs\docs\assets\cw_017.gif" style="zoom:67%;" />

- To map a keyword from utterance to the entity, select the required keyword and click **Add an entity for “”** button. 
- Select the relevant entity from the list.
- It will map the keyword to the relevant entity and help the AI bot to identify similar utterances.