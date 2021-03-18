---
id: workflow
title: Workflow
sidebar_label: Workflow
---

An AI bot workflow starts with a welcome message, extends to an initial question, presents relevant responses, enables the customers to respond, extracts the required information and then displays a message that ends the conversation.

This topic explains the steps for creating a conversational flow between a user and a bot using the Workflow Builder tool in the CogniAssist bot Builder platform.

Select **Workflows** ![](assets\CA_032.png), it directs you to the **Workflows** screen.

![](assets\CA_033.png)

This platform allows you to create a new workflow and modify the existing workflows.

### Create New Workflow

Click the **+ New Workflow** icon ![](assets\CA_034.png) to create a new workflow for your AI bot. The **Add New Workflow** pop-up screen will open for you to define the workflow settings. 

![](assets\CA_036.png)

Provide the required details in the below field to create a new workflow.

| Option            | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| Title             | Provide a title for your new workflow. Example, Bill payment. |
| Exported workflow | Click the **Choose File** icon to import the workflows, which is already exported from the same project or from a different project. |
| Flow Resume       | Select the **Flow Resume** check box, if you want to backtrack the history and resume to the previously entered interactions to help you control the AI bot's conversation flow. |
| Enabled           | Select the **Enabled** check box to activate the workflow. This check box is editable only if the initial version of the workflow is ready. |

Once you provide the required details, click **Create Workflow**. It creates a new workflow. You can modify, download and delete the workflow as shown below.

![](assets\cw_020.gif)

Click on the required workflow title, it directs you to the workflow builder as shown below.

![](assets\CA_037.png)

### Chatbot Actions

**Welcome Messages**

The welcome message is the starting point for all AI bot workflows and it starts the conversation automatically with the user. Example, Welcome back! How may I help you today?

**Questions**

After greeting the user, the AI bot will ask a question to find out the user intention. Example, Please let me know if you have any questions on our product.

**Outputs**

Once the chatbot asks a question, it will display several multiple-choice options. Each option leads to a unique set of responses and information gathering. Example, Select the topic from the options - send money, transaction status, insurance.

**Responses**

After the user selects an option from the list, the AI bot will respond with a confirmation message. You can create your own customized responses. Example, I can help you with that. Please provide your transaction ID.

**End Messages**

Once the AI bot receives the information from the user, it will display an end message. Example, Click OK to know the transaction status.

### Configuring Workflows

By default, it displays the **start** workflow step. Click on the **start** workflow to begin with the workflow configuration. Once you click **start**, it displays the below pop-up screen.

![](assets\CA_038.png)

#### Trigger Intents

Adding an intent is the first step to start a workflow. You can fetch the pre-defined intents in this section to trigger the particular action. Type the intent name in the **Trigger Intents** field and select the intent from the list.

If the user query matches the particular intent, it triggers the bot response.  A sample trigger is shown below.

![](assets\cw_021.gif)

***Note*** -  If you want to add a new intent, then select **Utterances** under the **Training** module and add the new intent. After adding the new intent, you can retrieve the same here.

#### Output Ports

The **start** workflow has a single output port by default. You can connect to the next node of the workflow using the output port. A node is used to gather or show information from or to the user.	

### Add new workflow step

Click the **+New Workflow Step** icon ![](assets\CA_039.png) to add a new workflow step. It displays the below list of options.

1. User Interaction
2. Logic Step
3. API Call
4. Send E-Mail
5. Live Agent Transfer
5. S3 File Upload
6. REST File Upload

#### User Interaction

Once the user triggers a particular intent, the bot should relevantly respond to the user. You can customize the bot responses here. Select **User Interaction** from the list, it displays the screen as shown below. 

![](assets\CA_040.png)

It displays the user interaction screen with the below options.

1. Responses
2. Slots
3. Code
4. Output Ports

##### Responses

- To add a bot's response to the user, click the **+Add Response** icon ![](assets\CA_041.png)under **Responses**. It displays the **Responses** tab as shown below. 


![](assets\CA_042.png)

- Enter the relevant bot response in the above text box. 

![](assets\CA_043.png)

- If you want to add a multi-line response,  click  the **+Add Response** icon ![](assets\CA_041.png) to add another response to the user.

![](assets\cw_022.gif)

Click the **Add** icon ![](assets\CA_054.png)to customize the response. It displays the below options.

![](assets\CA_055.png)

###### Buttons

Buttons provide a defined set of options, which enables the user to select the options in a convenient way. It helps the bot platform to find and answer the user query with high accuracy. 

Click **Buttons**, it displays the screen as shown below.

![](assets\cw_025.gif)



**Payload** - 

- You can provide a button title for the user's convenience. When the user clicks the button, the payload value is processed in the back end. For example, the button title is defined as "**Yes, please**" and the payload value is defined as **yes**. When the user clicks the **"Yes, please"** button, the payload value **yes** is processed in the back end to maintain simple logic process.
- You can also trigger an intent in the payload field. You have to provide the intent name in the format **/intentionname**. Example, /default/affirm.

**Quick Replies**

Chatbot offer users, a simple way to reply to a message through quick replies. The user can reply to the bot in just one click, instead of typing it. Quick replies are optional.

- Click the **+** icon ![](assets\CA_045.png) to add quick replies. 

![](assets\CA_048.png)

##### Slots

Slots are the variables which enable your AI bot to categorize and interpret the users’ query. If the user says, “I want to pay bills,” your bot first has to understand that the user is requesting for a bill payment activity. Next, it finds the slots in the user query to to find out what kind of suggestion it should give.

Ultimately, slots let your bot to find the appropriate matching answers to your user’s intent and relevantly responds.

Example, your bot would identify the statement as a #pay_bills intent with a @payment_type slot and a “credit card” value. From there, your bot can proceed with the credit card payment and then relevantly responds to the user.

- To define the slot settings, click the **Slots** tab. It displays the screen as shown below.

![](assets\CA_044.png)

**Slots**

- Click the **+** icon ![](assets\CA_045.png) to add a slot.

![](assets\cw_023.gif)

- You can provide the below details to define the slot settings.

| Option   | Description                                                  |
| -------- | ------------------------------------------------------------ |
| Required | Select the Required check box, if you want to keep the slot information as mandatory. Example, the slot name is given as **bankname**. So, the bot proceeds further only if the user provides the bank name. |
| Name     | Enter the slot name. Example, bankname. The slot names should not contain space. |
| Entity   | Select the entity name from the list. The list displays the custom and default entity types. |
| Is List  | Select the **Is List** check box to accept the user's response in a list form. Example, if the bot asks the user to provide the mobile number, and the user provides 2 mobile numbers, the bot will accept both the values. If the **Is List** check box is not selected, the bot accepts only the first mobile number. |
| Persist  | Select the **Persist** check box to save the slot information in the bot's memory, which can be used later when the user asks the same query. |

**Fallback Response**

If the user invalidly responds, the bot has to provide a fallback response. 

- Click the **+** icon ![](assets\CA_045.png) and add a fallback response.

![](assets\CA_046.png)

***Note*** - If you didn't define the fallback response, the bot displays the default fallback message "invalid response".

##### Code

You can define code related details in this section. 

- Click the **Code** tab and it displays the screen as shown below.

 ![](assets\CA_047.png)

##### Output Ports

You can connect the output port to an input port of a different node. 

- To define the output port settings, click the **Output** tab, it displays the screen as shown below.

![](assets\CA_049.png)

- You should provide the below to define the output settings.

| Option    | Description                                                  |
| --------- | ------------------------------------------------------------ |
| Port name | Enter a port name.                                           |
| Condition | Enter the condition to validate the user input. Example, if the condition is given as **text == "India"**, it validates the value **India** with the user input to proceed further. |

#### Logic Step

You can execute programs and add a logic step after a node using this option. select Logic Step from the list, it displays the screen as shown below.

![](assets\CA_051.png)

#### API Call

You can access the data or functionality of another application from your bot building platform using the API call option. Select **API Call** from the list, it displays the screen as shown below.

![](assets\CA_052.png)

#### Send E-Mail

Select **Send E-mail** from the list. It displays the screen as shown below. You can add an e-mail workflow. When this action is triggered, an email is sent to the recipients with the slot values such as transaction status, date, country name, etc.

![](assets\CA_050.png)

| Option         | Description                                                  |
| -------------- | ------------------------------------------------------------ |
| recepients (,) | Enter the recipients email ID. Each email ID should be separated by a comma. |
| Subject        | Enter the subject. Example, transaction status.              |
| email body     | Enter the information which is useful to the user. Example, Name, country, etc. |

***Note*** - You can retrieve the slot values using the below format **{slot_values}**. Type a slot name inside the braces {} to retrieve its value. Example, {country}. It will automatically retrieve the country name of the user in the email body.

#### Live Agent Transfer

Live agent transfer nodes are used to transfer the flow to a human agent.
Select the live agent transfer option from the new workflow step dropdown.

![](assets\live_agent_transfer.png)

selecting live agent transfer will open up the live agent transfer node as shown below.

![](assets\live_agent_node.png)

Inside the queue name specify to which live agent section the flow is to be transferred. for example mention the live agent associated with sale if the flow should be transferred to the sales section.



#### S3 File Upload

*for future purpose*

#### REST File Upload

*for future purpose*

To end the workflow step, select the **End Step** check box ![](assets\CA_056.png)and save the workflow.

Once you define conversational workflow, click the **Save** icon ![](assets\CA_98.png)to save the workflow. You can check the below basic workflow of a bill payment activity.

![](assets\CA_053.png)

Select **Enabled** check box in the **Edit** Workflow pop-up to activate the workflow.

![](assets\cw_024.gif)

Once the conversational workflow is complete, you can deploy the AI bot.



