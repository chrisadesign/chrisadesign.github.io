---
layout: post
title: Designing internal services, using the GOV.UK Design System, and one thing per page
---

I wanted to share some thoughts on designing for internal (caseworker) services in gov as I’ve heard from many people, in many departments across multiple projects, that the [GOV.UK Design System](https://design-system.service.gov.uk/) is not suitable for internal/caseworker products. This is usually followed with something about the recommendation to start with one thing per page.

**Important note:  
This is not an attack or condemnation of anyone or any team.**

## Where to start

The first thing is that the service manual has [design guidance for services for government users](https://www.gov.uk/service-manual/design/services-for-government-users), which says:

> Start with the [design guidance in the Service Manual](https://www.gov.uk/service-manual/design).

…which would be to utilise the Design System patterns and components until you find they don’t work. Even for external services there’s no hard and fast rule that you have to use all of them, what you do have to do is research and evidence why they don’t work.

The guidance also say:

> For example, a user of an admin system might need to repeat and switch between tasks quickly [which] might mean it’s not appropriate to apply a [one thing per page](https://www.gov.uk/service-manual/design/form-structure#start-with-one-thing-per-page) approach on all pages.

…so it actually calls out one thing per page probably not being appropriate for these products.

## More on one thing per page

The [one thing per page guidance in the Design System](https://design-system.service.gov.uk/patterns/question-pages/#start-by-asking-one-question-per-page) is to “start” with that. Like above, it’s fine if it doesn’t work and you need to move away from it even on external services.

The other point about one thing per page is that the “thing” isn’t an input, it’s a task or decision that needs making. If that thing needs multiple inputs to finish then that’s fine (*again* in external services as well as internal ones).

Last up is that that one thing per page guidance is actually just part of the [Question Pages Pattern](https://design-system.service.gov.uk/patterns/question-pages/) and more than that, the Question Pages themselves are just one of many patterns as well as components and styles. Those things come together to make the Design System, and while it might not be appropriate to use one pattern in our internal products we can still utilise the others.

And we totally should use those other things! They give us so much, even just as a platform to build more specific caseworker focussed work. We get an accessible, usable collection of designs and code that has been tested and researched and will be maintained and updated. This will let us to save so much time by not having to research and build it all ourselves.
