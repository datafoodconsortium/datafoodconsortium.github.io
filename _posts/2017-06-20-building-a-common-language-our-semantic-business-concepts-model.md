---
lang: en
layout: post
title: 'Building a common language : our semantic business concepts model'
description: A first version of our business concepts ontology
auteur: Myriam Bouré
img: "img/plugs.jpg"
comments: true
date: 2017-06-20 11:56
img_credit:
- name: Kiddo
  url: https://upload.wikimedia.org/wikipedia/commons/e/ed/Israeli-type-H-plugs-and-socket.jpg
  license-name: Wikimedia Commons
  license-url: 'https://commons.wikimedia.org/wiki/Commons:Licensing'
---


## June, 2017

After we described some first use cases that helped us frame the perimeter of what we wanted to share between platforms, now comes the time to work on the standard that we need to implement in order to make our platforms talk to each other and share information. It’s always good to remind the intention behind that work : to make the life of the producer engaged in direct sales / short supply chains easier, and make this new decentralized food system more efficient by finding new ways of cooperation (on logistics for instance)

## What is that “standard” ? And an ontology ?

With my  non-tech background, I like to describe a standard as a “common language”. When you talk of a tomato, and I talk of a tomato, do we talk about the same tomato ? Or do we mean different things ? Maybe I mean a cherry tomato and you mean a beefsteak tomato !

Or when I talk about an “order cycle” to design the time period when buyers can make their order, and when you talk about a “sale”, do we talk about the same concept ? Maybe we do but we just don’t use the same term… what could be a common way to describe our business, that we all agree on ? That is a standard :-)

Then by creating links to that common standard, we will be able to discuss with one another. It doesn’t mean we will need to change our own language, the standard operate more like a translator, and a connector ! A standard is an infrastructure, whether it be physical or digital.

An ontology is then just a machine readable version of a standard. So this is what we need so that the computers can do the job and talk to each other, share meaningful informations to make the life of producers easier !

## Two approaches

There are two ways to envision the implementation of a standard :

1- Look for the closest existing standard and make you fit in, eventually try to make it evolve

2- Start from scratch and build a custom standard, then eventually converge with the most meaningful existing standard

In our case, we looked for existing standards, but we felt from the beginning that no one was answering our need. We looked at generic “business ontologies”, like schema.org, or valueflows. It seems to us pretty far from our daily business activities and we thought we needed some reflexion to understand our business, and put our own common business description on a paper. So we chose the second approach, with the idea that afterward, we would like to converge and merge our work with an existing more generic business ontology.

## The business concepts and their relationships

So we started by describing the business concepts we were working on every day :

What ? The products that producers grow/transform and that distributors sell, stock, catalogs, baskets, parcels...

Who ? The distributor hubs, producers, suppliers, customer, hub operator…

How ? Orders, transactions, delivery and payment methods...

Where ? Shop, pick-up point, delivery zone, basket aggregation point...

When ? Sale session, delivery window, receipt date…

We needed at least 4-5 iterations to manage to describe things in a way that made sense to all of us, and taking into account the diversity of the models.

Here is the list of concepts we came up with (click on the image to see the full document) :


_Comment:_ we chose for the moment a Creative Commons license that doesn’t allow to modify the work. Indeed, the interest of standardization is to build a common standard, so we want to iterate and make the standard evolve, with a collaborative process and governance. But we want the future adopters of that standard to join us and work with us in the evolution of that common standard.

## Why do we talk about a “semantic business concept model” ?

The idea behind the semantic web is that data are all connected to each other, refer to each other, so they are interconnected and interdependent. That makes data smarter, as you can travel among the data world by following all those connexions. You can check [wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) which is an good example of semantic data.

## About the product ontology

Lots of actors have built products ontologies. Some are pretty retail oriented, like the [GS1 France products classification](https://www.gs1.org/gpc/browser), for instance. Some are really agronomically oriented, like [Agrovoc](http://aims.fao.org/fr/agrovoc). But few really mix both. We only found [UNSPSC](https://www.unspsc.org/) which is built and maintained by GS1 US. That could be a start, but we wanted to have a deep reflexion about “how do we make sure, when two machines exchange information about a product, that they talk about the same product? We need a “unique ID” if we want that to happen.

There are three ways to envision products interoperability :

1- **One to one mapping**, like in a zappier mode.  This is a fully decentralized approach.That implies that every platform need to map itself with the other platform they want to be able to exchange product information with. It could solve a punctual need, but won’t enable to really get machine readable cross-platform data to build mutualized logistics services for instance.

2- **A tree approach**. It means we agree on a common “pivot taxonomy” that we map our own taxonomy with. It is a centralized approach but you can see that as a common, with a collaborative governance and maintenance of it. The problem here is that if we want the platforms to be interoperable we need to map every product with the more detailed level of the taxonomy, as every platform might classify the products differently. And the issue is that this “more detailed level” differs from country to country and product to product. In France for example we have a large variety of cheeses. If we ask a German cheese maker to select the product among this detailed list, he will be pretty lost… same for the German beers, that are much more detailed than in other cultures !

3- So the approach that best seems to fit our need is a **“facets approach”**, or **“faceted classification”**. Here the only thing that we have to agree on are the different attributes that we need to describe a product (product type, nature of the product, label, unit of measure, packaging, producer…) and the different values that an attribute can take. For example, on the “nature of the product” attribute, we could use the Agrovoc ontology for varieties. That way, every possible combination is a unique ID that will enable product informations to flow from one platform to the other. We are not sure yet if UNSPSC is built that way, so we explore different directions.

## We decided to narrow down our first prototype.

In all that reflexion, we realized that our first idea of building a prototype as a directory to look to products, open sales session, hubs, etc. was far too large ! We decided to narrow down our prototype to a simpler use case : the fact for a producer to be able to upload/update his product catalog in multiple platforms at once, by entering the info in just one location.

## Next step

Now that we have a first version of our business concepts ontology, we want to publish it, share, and get feedback so that we can iterate on it. Also, we are envisioning various options to structure our consortium in a way that will enable it to operate on a longer term. We are discussing with different standardization players, as we are conscious that the work of maintaining and updating on a regular basis that ontology is not trivial. We don’t want to work alone on our side, we want the work we are doing to converge with more generic business ontologies, and we hope we can contribute in evolving those ontologies with the specific reflexion we had on local / direct / short supply chains business concepts. Of course, we continue to move on with the prototype and will now need to find the good technical solutions to implement this standard. Get ready for the next episode in a few weeks !
