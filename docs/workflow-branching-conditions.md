---
id: branching-conditions
title: Branching
sidebar_label: Branching
---

It is possible to give **branching conditions** in the output port section available in the workflow step.
![](assets\outport.png)

Let's look at this in detail with a small ***example***.

The picture below shows a simple workflow using user interaction nodes.
![](assets\branching_workflow.png)

Now lets open the user interaction node and set up branching menu and conditions.
Here in the below picture you can see buttons and its respective payload.

![](assets\branching_menu.png)

Now lets add some simple branching conditions.

![](assets\branching_condition.png)

Here the state changes only if the payload matches the branching conditions.
Meaning the bot traverses to the first state if the payload **pediatric** matches the condition **text == 'pediatric'**.

Now for the last state **text not in ['pediatric','youth','middle']** is another way of giving branch conditions. This can also be done as **text != 'pediatric' and text != 'youth' and text != 'middle'** or simply **text == 'elderly'**.


![](assets\branching_response.gif)

Like this there are multiple ways you can give branching conditions.
Branching with slots can be done using **slots.slotname == condition** in the output Ports.

Like the same way We can also branch by matching regex patterns. 

Conditions can be given in the Output Ports of the start node to specify the respective workflow is associated with which **communication channel**.

That is we can specify from which channel we are getting the request.
![](assets\branching_channel.png)
some example channels can be **rest, socketio, twilio etc.** 

[Click here to read more on supported channels](settings-channels)

you can refer [here](branching-rule-syntax) for complete syntax
