# Scenario 1 Data Platform Ordering

![Architecture](../Chapter%206:%20Enterprise%20Usage/platform-high-level-picture-automation.drawio.png)

## Introduction
In a new platform we want to use any kind of automation tool to easily enable teams to use central managed terraform repositories and more functionalities. The key here is to not manage everything centraly, but to give the teams as much freedom as possible. Here in this platform the key parts are giving the option to template following things:

 - Terraform repositories
   - Basic infrastructure which uses central terraform modules
   - Extendability of terraform with custom needs
 - Access handling
   - Access to central github actions which create and manage access based on groups
 - Key Value Store of configuration
   - Place foreach setup to configure and save settings to be used by all repositories
 - Deployment location for code
   - Ability to create repostories which are attached to the deployed cloud infrastructure to have easy CI/CD
 - API Interface for ordering