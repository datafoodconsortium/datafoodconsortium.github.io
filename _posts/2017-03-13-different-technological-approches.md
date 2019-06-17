---
lang: en
layout: post
title: Interoperate our platforms… what does it concretely mean? How can we make it
  happen?
description: 'Starting to envision the data architecture: the different steps of the
  data and the impacts of different technological approaches'
auteur: Myriam Bouré
img: img/data.jpg
comments: true
date: 2017-02-22 10:17
img_credit: []

---
**February 22nd, 2017. Second meeting.**

Before we start getting our hands dirty on a concrete prototype, we wanted to take the time to build our collective awareness on what it means to interoperate our platforms. What can be the impact? What can be the technological solutions we could use? So that we can all engage with awareness.

Here is how we formulated the intention for that second session :

_“Reach a shared consciousness about the possible solutions to interoperate our platforms and their respective impacts, and start to envision an architecture on how “products” and “orders” data could be described, filled in, shared and accessed.”_

## The different steps of the data

To simplify daily management of products catalogs for farmers and food hubs, we need platforms to be able to share data. For example, a producer working with various food hubs using different platforms should be able to manage his inventory in one platform and then allow the other hubs to access and display it (or part of it) on their own shop front. What is the life cycle of data and what do we need to do at each stage to be able to share it?

**1. Describe.**  
To enable our platforms to share data that can be used by other platforms, we need to adopt a common vocabulary, a standard. That doesn’t mean that every platform will need to change its terminology. That means “when you talk about a tomato and I talk about a tomato, are we talking about the same tomato?”. The solution would be to define a meta-ontology encompassing all the specific ontologies used by every actor.

**2. Fill in.**  
Data are currently entered in a specific way and format, depending on each platform. No need to make that evolve to ensure interoperability, APIs will make it possible whatever the origin format. It might be interesting however, to consider options to enrich the data through a semantic format. Semantic data makes it easier to connect with external databases (see [wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) / [dbpedia](http://wiki.dbpedia.org/)) and make the data smarter.

**3. Share.**  
Given the meta-ontology described, every platform can set up an API that will enable to “match” fields used by different platforms and display information from distant databases. This stage has more impact on how platforms and applications are built. The platform will now need to query not only its own database, but also distant databases through the API. Can it be done in a dynamic way? Is a proxy needed to copy the data into the platform database before displaying them?

**4. View.**  
When the data has been “called” through the API and is ready to be displayed in the platform’s front end, the last step is to display it so that it can be read by the client in his browser. If the platform wants to display new field they need to add them, but else, no specific work needs to be done on the platform side.

![](/img/webdistribueenglish.jpeg)

## Which data are we talking about and what questions does that raise?

It’s pretty easy to imagine the tomatoes of Charlie’s Grow Organic, who manages his catalog in The Food Assembly, displayed on a buying group shopfront using Open Food France. But what about “orders data”? If I buy tomatoes in my buying group using Open Food France, how can Charlie’s Grow Organic receive the order and process it? Does he receive the order in his Food Assembly interface? Does he receive an email notification and need to go in Open Food France to see and process the order? Does he only receive an email? Does he use a third party interface where he receives orders from any platform and process them there? The last option would probably be the most logical. But then what should be the governance of that third party interface?

So yes, we will start by describing a meta-ontology that we can use as a standard to share information about products. Each platform will need to build an API respecting that standard if they want to be interoperable with the other ones. That will be a first step, and we’ll see then how to move forward. Butlet’s keep in mind what we do that for: to simplify the life of the farmers and build a decentralized and efficient food system.

## About semantic data: the different technological approaches

If the players around the table want to evolve toward semantic data and benefit from the possibilities it opens in terms of connectedness, there are 4 main technological possibilities that should be considered all along the project.

1- An external shared solution where data are filled in and can then be displayed in any platform. For example, the producers catalogs are managed in a third party producer application, all the data are entered there and then can be displayed in all the applications that the producer has authorized.

2- A shared solution deployed internally by each actor. For example a module/plug-in that enables data to be entered in every platform but that is connected to a database that any platform can then access (given permission from the producer)

3- Each platform chooses how the data are filled in and just deploy the API to share them.

4- A third party “pivot” tool called “semantic bus” is implemented and interfaced with every platform, so anytime a data is entered in a platform, it is “processed” by this semantic bus and can be reintegrated in a semantic format and/or shared given the rules agreed upon.

Some of those approaches are based on a shared common, a solution that we decide to deploy together and use, because it benefits us all. Of course in that case we will need to build a collaborative governance around it. No choice need to be made at that stage, we will see when we move forward on the prototype what makes more sense, and the solution chosen can change when we move forward and work on other cases. But I think it does make sense **to ask ourselves at each moment the question**: 

> **What do we need to manage in common to make the life of producers easier?**

## Next steps

In our next session we will get our hands dirty, discuss about potential use cases and chose the one we are going to work on for our first prototype :-)

Want to take part in the discussion ? [Contact us](http://datafoodconsortium.org/#contact) or leave a comment !