# Chapter 2: Basics

## What are Github Actions?

Interface to execute anything you want and have hosted in your repository with easy integrations to git events. General tasks are building applications, testing, handling releases, deploying infrastructure and many more depending on the use case!

## How does Github Actions work?
Basically github action is a piece of software which can run on any device and will execute a shell with the steps you tell it should execute. This simple concept enables you to use any programming or scripting language you want. Installing new tools can be realized by using steps that install the new tool or directly going into the runner and installing the tool.

## What do I need to start?
Starting point on github.com is only the repository itself. Runner and installing tool is taken care by github.com and first actions can be started right after creating a repository.

## Important point with github actions:
- Secret handling
  - Secrets can be added directly to the repository or the organization
  - External secret stores are not advised cause build in support is great!
- Usage
  - Cost of github action is handled after execution time so long running actions are costly
  - Keep it stupid simple
  - Smaller reusable actions are better than long all in one actions
  - Actions can be chained
- Reporting
  - Successful runs can be tracked and ribbons added to git repository
- Steps
  - Big repository on github.com about predefined steps from verified providers
  

  
# STARTING IS THE FIRST STEP
