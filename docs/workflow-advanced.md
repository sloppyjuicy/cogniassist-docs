---
id: workflow-advanced
title: Advanced Workflow
sidebar_label: Advanced
---

## Events
Event is an easy way to trigger any bot skill from anywhere else directly without using NLP trigger.

Events can be triggered  by:
- Initial payload set in Chatbot UI configuration 
- Buttons
- External Events
- workflow Script

You can trigger events directly in the chatwindow by prepending '/' to any event name

### Default Events
CogniAssist allows you to customize your chatbot by making use of the default intents. It can be used as trigger points to workflows, payload for interactive elements and much more

![](assets\trigger_events.jpg)


#### default/welcome
The default welcome intent is automatically created when you create a bot. This intent is preconfigured to handle the generic welcome smalltalk.
You can set this event as a trigger intent to any workflow to replace the welcome smalltalk

#### default/restart
Triggering this event will cause the chatbot to reset all the slots and active memory of the current session

#### default/live_agent_trigger
This event is used to trigger the live agent transfer. You need to have a valid Live Agent configured for this to work.

#### default/affirm
This event will be parsed as a True/Yes by chatbot. You can set this as a payload for interactive elements

#### default/deny
This event will be parsed as a False/No by chatbot. You can set this as a payload for interactive elements

#### default/fallback

This is the event used to trigger fallback scenario of your chatbot. You can set this event as a trigger intent to any workflow to do some API call or custom fallback handling.