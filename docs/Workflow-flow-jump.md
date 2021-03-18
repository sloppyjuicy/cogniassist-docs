---
id: flowjump-node
title: Flow Jump
sidebar_label: Flow Jump
---

The flow jump node is used inside a workflow for jumping over to different workflows.

Let's understand the use of a flow jump node with a simple example.

First let's create 2 workflows as shown in the below pictures.
click [here](workflow) to see on how to create a workflow.

![](assets\flowjump_workflows.png)

#### Setting up the Pediatric workflow
Create a workflow as show in the picture below.
![](assets\flowjump_pediatric_workflow.png)

now let's configure the human interaction node.

![](assets\flow_jump_redirect.png)

tick the end step checkbox available inside the output port section.Save close the workflow to create the second one.

#### Setting up the Test workflow
![](assets\flowjump-test-workflow.png)

Flow jump node can be selected from the workflow step dropdown inside a workflow

![](assets\flowjump-selection.png)

configure the human interaction node as shown

![](assets\flowjump_menu.png)

![](assets\flowjump_condition.png)

Finally let's configure the flow jump node.

![](assets\flowjump_node.png)

In the flow jump node specify the workflow name to which you want to jump and the target node from the workflow.

![](assets\flowjump_response.gif)


