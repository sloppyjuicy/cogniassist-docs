---
id: workflow-api 
title: API Call Integration
sidebar_label: Api node
---

### API Call

You can access the data or functionality of another application from your bot building platform using the API call option. Select API Call from the list, it displays the screen as shown below.

![](assets\apicall.png)

The API Call screen is displayed with the following options.

1. API Builder
2. Slots
3. Output Ports

#### API Builder

To call the API, enter the relevant url and details in the API Call node as shown below.

![](assets\apicall_1.png)

You can add HTTP headers by clicking the **+** near the **HTTP Headers** ![](assets\http_header.png)
There you can add the key and its value in the space provided.

To add JSON Payload, tap the **JSON Payload icon** ![](assets\json_payload.png)

There is an option to add Timeout Request and No. of Retries.

![](assets\api_call.gif)

#### Slots

Slot name will be automatically added while adding the reference name. Once you save the reference name, the slot name will be automatically passed as the id. If you change the reference name after saving, the slot name will get changed but the id will not change. 

![](assets\api_slots.png)

#### Output Ports

You can connect the output port to an input port of a different node. 

- To define the output port settings, click the **Output** tab, it displays the screen as shown below.

![](assets\CA_049.png)

- You should provide the below to define the output settings.

| Option    | Description                                                  |
| --------- | ------------------------------------------------------------ |
| Port name | Enter a port name.                                           |
| Condition | Enter the condition to validate the user input. Example, if the condition is given as **text == "India"**, it validates the value **India** with the user input to proceed further. |
















