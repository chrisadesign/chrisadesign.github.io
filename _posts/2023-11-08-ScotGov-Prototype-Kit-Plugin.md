---
layout: post
title: GOV.UK Prototype Kit plugin for the Scottish Government Design System
---

A couple of years ago I created a fork of the prototype kit with the Scottish Design Dystem (ScotDS) embedded in it. I've not looked at it since and it's likely very out of date, plus things have moved on with the prototype kit which now has plugins, so I've had a crack at creating a plugin to bring the ScotDS into the kit.

## How to use

Once you have a version of the prototype kit installed,
- open a terminal window at that folder and run **npm i scotgov-prototype-plugin**
- create a **settings.scss** file in **app/assets/sass** and add **$govuk-global-styles: false;** to it
- open **app/views/layouts/main.html** and change the extend from **"govuk-prototype-kit/layouts/govuk-branded.njk"** to **"/scotgov-prototype-plugin/scotgov-template.njk"**
- run **npm run dev** as usual

That should get you up and running, the ScotDS has a different structure and class names so you'll want to update the default code in the index file or things will look at bit wonky.

I've set this up quickly (and unofficially) so there might be bugs, but I'll hopefully be starting some work within ScotGov soon so this might evolve as I need more from it.

[View the plugin npm package](https://www.npmjs.com/package/scotgov-prototype-plugin).
