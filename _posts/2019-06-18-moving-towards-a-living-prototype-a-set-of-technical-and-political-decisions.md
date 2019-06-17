---
lang: en
layout: post
title: 'Moving towards a living prototype : a set of technical and political decisions'
description: ''
auteur: Myriam Bouré
img: img/visueldfc.jpg
comments: true
date: 2019-06-18 00:00:00 +0200
img_credit: []

---
**June, 2019.**

It’s been almost a year since we published the first version of the DFC ontology. Since then, we have tried to find money to move the project forward, and especially, to be able to hire some technical skills to help us on the tech side and develop a living prototype.

This has taken us quite a lot of time, and we have only partially achieved our goal. **The French** [**Region Ile-de-France**](https://www.iledefrance.fr/) **has agreed to support us over a three year project** for around 150K€, but we are still looking for co-funders as they can only finance half of the bills.

![](/img/Logo-quadri-couleur-1.jpg)

Let’s remind also the financial support we already have from [**Fondation Daniel et Nina Carasso**](https://projets.fondationcarasso.org) and [**Fondation MACIF**](https://www.fondation-macif.org/), who finance the time spent for the coordination of the project.

![](https://lh6.googleusercontent.com/X9LUsQ1W8E0DBqRIRYwZ21NFRNbRdHIM6868ByLaLVyC7rIWqSnVZkBljQHIL_niVxwr0ngFI5ZDOl1JFz_-XNPHsLl2jRGLWqgxKPeufIhRueHWvInX-1XxdUBQTDw-hXjLkLlJ =194x72)

 ![](https://lh6.googleusercontent.com/hHGQqxA_53AacqO2lbDrQHfYTc3WGtudemaBMPoFm0S61TdK9-Z8eh2vjRv9fvE12k2mVGTgHEbQtnaLdITWuwkugv4MxVNrFE0Y6ubmYe0nfxpta-SBzUKNrhwbdn8_tCSWYoIX =121x121)

This has still enabled us to start working with [Simon Louvet](http://semapps.virtual-assembly.org/detail?uri=http%253A%252F%252Fdata.virtual-assembly.org%253A9050%252Fldp%252F1518445159943-2777738335754558), who is a member of the [Virtual Assembly](https://www.virtual-assembly.org/) and has worked on several semantic and distributed web projects.

We ran various sessions on communication protocols and architecture of the prototype. Transition from silo-based applications to interoperable architectures is complex ! Our ideal is not easy to reach and will need some steps.

> **_>>> We also improved our documentation, you can now find_** [**_through this Gitbook_**](https://datafoodconsortium.gitbook.io/dfc-standard-documentation/) **_the current semantic and technical specifications of the DFC standard._**

## **Evolution of the ontology**

We had to evolve the ontology as we realized we needed a way to reflect that a given producer (agent) can have for the same product various item catalogs in various repositories. For instance, a producer who sell via 3 platforms will probably have 3 records for the same products, in 3 databases, maybe with some discrepancies…

We also added some concept to manage theoretical and real stock, and stock limitation that could be used to limit the quantity available for a given agent.

We changed a bit the [presentation](https://drive.google.com/file/d/1Ru1mJhko6jOoy1KkYbuxvd0wSCvfC26j/view?usp=sharing) to make it a bit clearer:

![](/img/Semantic_business_model-June2019.jpg)

On product ontology side, we only split the territorial origin into two sub facets.

You will find a description of the business and product ontology in the [semantic specification chapter of the documentation](https://datafoodconsortium.gitbook.io/dfc-standard-documentation/semantic-specification/business-model-and-ontology).

## **The technical architecture**

While working on a real life case, through the development of a first prototype, we could start listing technical decisions we needed to make and potential solutions. Those decisions concerns things like protocols, request processes, granularity, URL structure, gateways between protocols, serialization, transport layers, directionality, identification and authentication, right delegation, data storage.

The decision were envisioned in 2 phases, phase 1 being more like a “transition step” we need to take to learn and see how to move towards something a bit more decentralized.

You will find all those technical design decision in the [technical specification chapter of the documentation](https://datafoodconsortium.gitbook.io/dfc-standard-documentation/technical-specification/overall-strategy-for-building-a-reliable-spec).

## **Product identification : our political decision to work with Open Food Facts**

[Open Food Facts](https://world.openfoodfacts.org/) ([Open Products Facts](https://world.openproductsfacts.org/) more generally) is a Wikipedia type project that aims at bringing back product information as a common. They develop on an iterative mode taxonomies to make product description easier. They do that on a community-based open process and attribute codification without the necessity for a producer to pay for a subscription (contrary to the basic GS1 model).

The reality in local food chains is that very few producers are willing to become GS1 members. Also, Open Food Facts invite people to share their product information as open-data. As DFC we don’t want to force the producers to share their data as open data but we want to make it easy if they want to.

So we took the decision, for the prototype stage, to use Open Food Facts product identifier as the DFC product identifier. We also decided to map and adapt our product ontology (the facets we use to describe products) to the Open Food Facts one, even if it’s not perfect. We are realistic that taxonomies are hard to establish and maintain, and we prefer to join a community and contribute to improve the “taxonomies as a common” that they are building, and use it. We will still have our own database to enable producers who don’t want to share their data as open data not to. But as we will use the same facets to describe products, and same IDs, that makes it super easy to migrate info from our DFC database to Open Food Facts one if a producer agrees to share their product information as open data.

## **The user experience of the prototype : what a mess !**

On the UX side, interoperability can be pretty complex. The application we are building as a first step aims at enabling a producer to “connect” on his “universal DFC catalog” all the products catalog she owns in various platforms that are part of this experiment. Those platforms will do some work to plug their application to the DFC standard.

So the producer will be able to “connect and import products items” from a first catalog. When they do the same for a second catalog, we will need to reconcile, so check if some products are already imported, thanks to the Open Food Facts unique product identifier, which is an EAN type code. It is actually the EAN if the product has one. If the product where already imported and some basic information differs we will need the user to resolve the potential conflicts.

Imagine… how are we doing that for a producer who sell through 3, 4, 5 platforms ?

It would be so much easier if the producer could have her unique catalog somewhere, and the platforms would read the information in it ! Ok. That’s what we are trying to build. I got it. But you can see through that illustration how complex it is to harmonize data from multiple sources.

Also, for the prototype, we made it simple regarding synchronization of data. If a product is modified in one of the source catalogs, it is not updated immediately in the prototype. The user will have to manually “update info from sources” to make a new import, and might have to solve new conflicts when she does that…

To conclude, I would say that this intermediate solution and experiment to try to build a single universal catalog FROM existing catalogs is a pretty hard task. We hope soon that the platforms will be able to read the info from that unique catalog. The producer could in that case manage her product information in one single place for all her clients and distribution channels. But we still have a long way to go !

## **Next steps**

You can follow the progress of the development of the prototype through the [Github project board](https://github.com/orgs/datafoodconsortium/projects/1).

We now enter a “production phase” where we organize the developments of the prototype through bi-weekly sprints. We will write a new post when a MVP of the prototype is ready !

In parallel we will keep on looking for funds to secure the continuation of the project. If you have ideas or see opportunities, please contact us at hello\[at\]datafoodconsortium.org :-)