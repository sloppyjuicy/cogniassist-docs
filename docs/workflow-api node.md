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

To call the API, enter the relevant url and details in the API Call node. 
Below given is an example of a bitcoin calculator which uses real-time excahnge rates which helps to find out exactly how much the Bitcoin is worth in different currencies.

![](assets\apicall_1.png)

In the above API url, **currency** is a variable which is already set as a slot name earlier and is parsing into the url using {{}}. In this way you can get the correspovalue of bitcoin for any currency.

- You can add HTTP headers by clicking the **+** near the **HTTP Headers** 
![](assets\http_header.png)

- There you can add the key and its value in the space provided.

- To add JSON Payload, tap the **JSON Payload icon**. ![](assets\json_payload.png)

- You can use slots to build your JSON Payload. You can type **'{'** for autosuggestions. 

- There is also an option to add Timeout Request and No. of Retries.

![](assets\api_call.gif)

#### Slots

Slot name is the result of API call. It is added in the **Slots** option. You can use the API result by just calling the slot name.

Slot name will be automatically added while adding the reference name. Once you save the reference name, the slot name will be automatically passed as the id. If you change the reference name after saving, the slot name will get changed but the id will not change. 

![](assets\api_slots.png)

#### Output Ports

- To define the output port settings, click the **Output** tab, it displays the screen as shown below.

![](assets\api_output.png)

- You can check the API status condition by providing the condition **api_status == true** or **api_status == false**. **api_status** is a variable and it will be defined in the code.
















