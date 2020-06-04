---
id: product-synonyms
title: Product Synonyms
sidebar_label: Product Synonyms
---

When you design a bot, they should have three parts:

- Slots
- Values
- Synonyms

Slots are the variables you give your program to let your bot categorize and interpret users’ input. If your user says, “I want to order a pepperoni pizza,” your bot first has to understand that the user is asking for an order. Next, to narrow down what kind of suggestion it should give, it finds the slots in the sentence.

In our pizza example, your bot would identify the statement as a #place_order intent with an @pizza_type slot and a “pepperoni” value. (We’ll get into what all that means in the next section.) From there, your bot can place the order for the correct pizza and then respond to the user with payment and order details.

**Ultimately, slots let your bot filter what types of answers will match your user’s intent and subsequently choose the correct response.**

You can provide different types of abbreviations for your domain terms or key products in this section. Select **Product Synonyms** <img src="assets\CA_030.png" style="zoom:50%;" /> under the **Training** module, it directs you to the **Domain Dictionary** screen.

![](assets\cw_018.gif)

Adding variation of abbreviations to a keyword helps the AI bot to develop personalized responses. Example, if the user says "I want to send money to John" and if the AI bot is already trained to identify a person's name from the user's query, the AI bot provides a personalized response.