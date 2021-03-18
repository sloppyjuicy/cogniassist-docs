---
id: code-editor
title: Code Editor
sidebar_label: Code
---

Inorder to write the code you can use either **Code** option in the **User Interaction** or **Logic node**.
If you are writng code inside User Interaction, there will be 3 options
1. On Enter
2. On Input
3. On Exit

![](assets\options.png)

- On Enter- preprocessing before asking user
- On Input- transforming user inputs
- On Exit - post processing setting stuff for the upcoming states


#### Set slot

You can set a value to a slot by using **set_slot** function inside the code editor.
	**self.set_slot('slot_name',slot_value, persist=False)**

- Above shown is the format of set_slot function.
- There are 3 parameters :
	1. slot_name : here you need to provide the name for the slot inside inverted commas.
	2. slot_value : here you need to provide the value of the slot.
	3. persist : by default this value will be False. If you want value of the slot to persist throughout the 
			   	 process then you must set **persist=True**.


#### Get Slot

You can get a value of a slot by using **get_slot** function inside the code editor.
	**self.get_slot('slot_name')**

- Above shown is the format of get_slot function.
- It has only 1 parameter
	1. slot_name : here you should provide the name of the slot from which you need value.

![](assets\set_slot.png)
![](assets\get_slot.png)

#### Send Message 

You can also send messages/responses to the user through code by using **send_message** function.
	**self.send_message(message=" ")**
- Above shown is the format to send response to the user.
- It has only 1 parameter and you can put your message inside the double inverted commas.

![](assets\send_msg.png)