---
layout: post
title: GOV.UK Prototype Kit plugin for the Scottish Government Design System
---

> Update 16 Nov 2023: I've updated the package to use the templates functionality of the kit, hopefully this makes the installation instructions simpler.

A couple of years ago I created a fork of the prototype kit with the Scottish Design Dystem (ScotDS) embedded in it. I've not looked at it since and it's likely very out of date, plus things have moved on with the prototype kit which now has plugins, so I've had a crack at creating a plugin to bring the ScotDS into the kit.

## How to use

Once you have a copy of the prototype kit installed,
1. open a terminal window at that folder and run **npm i scotgov-prototype-plugin**
2. run **npm run dev** as usual
3. create a **settings.scss** file in **app/assets/sass** and add **$govuk-global-styles: false;** to it
4. in the browser, navigate to the **Manage your prototype** section and go to **Templates**
5. create the required main layout at **/layouts/scotgov-main**
6. create and use one of the other templates as a basis for your prototype

I've set this up quickly (and unofficially) so there might be bugs, but I'll hopefully be starting some work within ScotGov soon so this might evolve as I need more from it.

---

[View the plugin npm package](https://www.npmjs.com/package/scotgov-prototype-plugin).
