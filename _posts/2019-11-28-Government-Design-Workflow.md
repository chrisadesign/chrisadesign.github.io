---
layout: post
title: My workflow for government design projects
---

One of the most common things I get asked by designers new to government is how to set up a new project using the [GOV.UK Prototype Kit](https://govuk-prototype-kit.herokuapp.com/docs).

> Update: I don't use multiple Heroku instances for versioning anymore, mostly because other team members find it harder to navigate. Instead I have a versioning system baked into my [fork of the prototype kit](/Prototype-Kit-Fork/).

There are already some great guides out there for publishing to Heroku, for example GOV.UK's guide [Publishing on the web](https://govuk-prototype-kit.herokuapp.com/docs/publishing-on-heroku). There's also guides for archiving versions of your prototype, for example Alex Torrance's article [Archiving versions of a prototype](https://designnotes.blog.gov.uk/2016/05/13/archiving-versions-of-a-prototype/).

My workflow is very similar, although I use the command line a lot less, and I think that makes it easier for people new to this. So I thought I'd share.

## Set up a repo on GitHub
Most departments I've worked with use GitHub for version control. I'm not going to delve into using git here but if you're new to it I highly recommend Alice Barlett's [Git for Humans talk](https://www.youtube.com/watch?v=eWxxfttcMts).

I use [Sourcetree](https://www.sourcetreeapp.com) rather than command line as I find a git GUI much easier to use and fix issues with. But whichever method you like, go ahead and create a new repo for your prototype.

[Download a copy of the kit](https://govuk-prototype-kit.herokuapp.com/docs/install) and push it to your repo (don't miss the gitignore hidden file in the folder).

## Deploy to Heroku
You can deploy to Heroku in the command line as covered in the GOV.UK guide, but there's a bunch of commands to learn, and time spent in the terminal, which can be daunting if you've never used it before. The good news is you can deploy your prototype using Heroku's website as well.

### 1. Sign in to Heroku
[Sign in to your Heroku account](https://id.heroku.com/login) or [create an account](https://signup.heroku.com) if you're new to Heroku.

### 2. Create a new app
On your personal apps screen your should see a list of any existing apps and a **New** button that will drop down with a couple of options. Select **Create new app**.

You'll need to choose a name for your Heroku app which will determine the URL for your prototype; for example, the name **example-prototype** would equate to **https://example-prototype.herokuapp.com**.

Finally set the region to Europe and go ahead and hit the **Create app** button.

### 3. Deploy your prototype
Select the **Deploy** tab. You should see a heading for **Deployment method** with an option for using GitHub. If you select this it will link your GitHub account.

Once you've linked your account you'll be able to search for your prototype repo and select the **Connect** button.

With your app connected to your repo you should now see an option near the bottom of the page to **Deploy a GitHub branch**. Go ahead and deploy the master branch. Even better than that though, is the option for **Automatic deployment** right above it. If you select the **Enable automatic deploys** button in that section your Heroku app will update any time you push to master!

### 4. Add a username and password
One more thing before you're done, select the **Settings** tab and you should see a **Config Vars** heading with a button to **Reveal config vars**. You'll need to add two keys, one for **USERNAME** and one for **PASSWORD** with a value for each.

Some departments have rules around what these should be, so check, but you don't have to worry too much about a strong password here. It's mostly to stop the public stumbling across your prototype and thinking it's a live service.

## Archiving versions
The guide on the gov blog about this uses tags on your repo to flag where a new version was started, and creates a new app based on it. I find that designers aren't generally aware of tags in git but usually have an understanding of branches, so I use them instead. Branches also have the advantage of being able to set up automatic deploys on Heroku.

I tend to create a new branch for each sprint's worth of work, along with a new Heroku app named similarly, for example **example-app-sprint1**. This means that changes don't affect ongoing research or internal reviews while I'm working on the next iteration.

Within the prototype I use the index file as a log of each sprint's work, with any changes and findings listed alongside a link to the Heroku app.

The process for this is largely the same as earlier:
* create a new branch, for example **sprint1**
* push your changes to GitHub
* create a new app on Heroku (I usually set the username and password the same across all apps)
* setup automatic deploys, selecting your new branch in the dropdown
* once the sprint is done update the index file and merge into master

That's it, if you have any feedback you can [reach out to me on Twitter](https://twitter.com/chrisnothanson).
