# Chapter 3: Hello World Action

## Action Code

All actions are written in basic yml language, that describe easy what the runner should do when the action is triggered. In this "Hello World" example we will go through the basic parts of the yml file and explain how each of that parts in a basic action are used.

But first a screenshot of the UI if you just use the default basic hello world example from github.com

![Hello World YML](../Chapter%203:%20Hello%20World%20Action/Hello_World_yml_start.png?raw=true "Hello World YML")

Also you can add small ribbons to show the last execution of the action with status (definable from which branch or event/trigger)

![Hello World](https://github.com/CloudNinjas/Github-Action-Learning/actions/workflows/hello_world.yml/badge.svg)

## Trigger ON Part

In this block you define when the action is triggered. Here option differ from events on the git branch like pull request or commit on specific branch or the easiest manual execution. 
(just as short help: manual triggers only show under actions-tab when the changes are either commited to the main branch OR when there is a second trigger based on the wanted git branch!) 

## What to do JOBS Part

The jobs part of the yaml file is the meat of the action and defines what the runner should do. Here we start with defining on which kind of runner we are executing, like our own self-hosted runners or on which image from the pooled runners from github.com. 

In the steps part we now declare what kind of workflow steps we want to execute. Here we either define everything that we want complete on our own in scripting or we use predefined workflow steps from the workflow repository to make our life easier. Best practise here is to use general workflow steps from providers that you do not need to care about handling the setup of tools and enviroments like versions/folders etc.. In github enterprise public available workflow steps can be added and whitelisted. From our example we start almost everytime with checking out the current repository in the git branch we are executing the action in. Afterwards doing some really small script steps with echoing a oneliner and echoing a twoliner script to show basic execution. 

What can be done in Actions is really up to your needs in automation and complete setups like customer ordering of services with a lot of external systems can be build. All in all it is a really simple CI/CD tool to be adopted that can handle all the needs you would have.
