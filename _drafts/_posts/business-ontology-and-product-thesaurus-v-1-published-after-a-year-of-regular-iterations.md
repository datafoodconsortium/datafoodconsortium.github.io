---
lang: en
layout: post
title: 'Business ontology and product thesaurus: v.1 published after a year of regular
  iterations'
description: Some tips to understand the v.1 of the DFC standard
auteur: ''
img: ''
comments: false
date: 2018-05-28 00:00:00 +0000
img_credit: []
---
## May, 2018. 

Since a year we’ve been working to build a common language in order to interoperate our platforms. With [Bernard Chabot](https://www.linkedin.com/in/chabotbernard/) we went from sessions when we theorized concepts and relations, to sessions with business actors to test our theoretical modelization and evolve it step by step.

We are now reaching a point where we are confident enough in our model to test it live. So we are releasing 4 documents :

* A pprj and owl file for business ontology. They encompass the main business concepts we manipulate in local food businesses.
* The associated glossary (we need to integrate the definitions into the above files, we keep that file meanwhile)
* A pprj and owl file for product glossary. Those files encompass what is needed to describe and identify products. They are meant to be connected to existing or home made thesaurus, but that will be for a further iteration.
* A pprj and owl file called “full model” that make the junction between business ontology and product glossary.

\[add links to Github\]

## How we have evolved since a year on business description

Since the v.0 we published last June, a lot of things have changed! It is really a journey to reach a point where we manage to cover all the use case of our businesses in a simple and consistent shared model.

Here is the image of the model we ended up with \[add Yed image\]

**Products:** 

* We have identified the different concepts of products we manipulate. As described in [this blogpost from November](http://datafoodconsortium.org/blog/product-ontologies-how-business-invariants-apply-also-to-the-food-system) we distinguished the product “need” (what I want as a customer), from the product “answer” (what I propose as a distributor to satisfy your need), from the product “supply” (what I propose as a producer that enable distributors to meet their promises to customers), all those products being manipulated without any “location” notion. 
* Then a producer identifies a location where their products are supposed to be when they become real product. We call them “localized products”, which is a combination between an ID product (what product it is) and an ID place (where it is). For instance, the potatoes of “Awesome farm” are in theory localized in the farm itself.
* When the potatoes get harvested they become “physical products”, real products that you can hold in your hand. A physical product is also always located somewhere, and belongs to a product batch.

**Transformation:**

* Some products are “composed products”, they are made of other products, processed in some way to make a new product, like a tomato sauce for instance. There is a theoretical transformation that plans a transformation process without any notion of where the products are located, the “recipe” that connects products with one another independently from where they could be. For instance as an artisan cookies maker I can tell that I put 100g flour, 20g chocolate, 2 eggs, etc. in my cookies. In that case I express the recipe in term of “functional products”, I need flour and chocolate. I can be more precise and tell which type exactly of flour and chocolate I use and talk more in term of “technical products”, like spelt flour T110. And I can even tell exactly the flour from which farmer I used in my recipe, so express the recipe in terms of other “supplied products”. This is what we call the “as planned transformation flow”.
* Then this recipe becomes something more like a “production workflow” that adds some notion of location. I have to move the tomato from “Awesome farm” to “TheKitchen”, the onions from “The Other Farm” to “TheKitchen”, etc. When all my components are in TheKitchen I can start the production process, cook, mix, bottle, etc. And get some jar of tomato sauce as output, which are located in “TheKitchen”. But this is still only a plan, a production map, I still don’t have the products, I’m just organizing and planning the operations. We realized when iterating that **transforming the nature of a located product was exactly the same flow as transforming the place where this product is supposed to be located**. As the located product is a combination of an ID product and an ID place, one flow was transforming the ID product, the other the ID place. So **we are treating transportation as a specific transformation flow**. Input will be for instance 100 x potatoes 1kg located in “Awesome Farm” and output will be 100 x potatoes 1kg located in “The Great Town Shop”.
* Then when physical products are concerned this flow becomes a “realized transformation flow”.

**Sales session:**

* A sales session aggregates some “offers” that an enterprise makes and that are specific to customer categories. The product offered can be, depending on the sales and marketing strategy of the distributor, a functional product (ex: tomatoes to stuff), a technical product (ex: beefsteak tomatoes) or a supplied product (ex: beefsteak tomatoes from Awesome Farm).
* The customer makes an order with various order lines in a specific sales session and choose a shipping option, that can be delivery (they are delivered to their home or business address) or pick-up (they need to collect the product in a location defined by the distributor) and a payment option among those defined by the distributor.
* The sale happens in a place that can be physical (a physical store) or virtual (an online store). Note that this works as well for a physical store: technically each day the store opens and close at a define time, and each day can be considered as a specific sales session. In the case of physical store sales, the shipping option is implicitly “collect on site”.

**Transactions:**

* When an agent has ordered products and products has been delivered through a last transformation flow (transport), the ownership of the product changes hands. The transaction is then officially happening and the previous product owner can invoice the customer.

## Product glossaries: the approach we choose

We studies different option for product glossaries/thesaurus. Our challenge is to **make sure we can identify uniquely products from one platform to another so that information regarding this product flow without friction.** As each platform has its own way of describing products, and its own logic, we choose to adopt a “facet approach” a little bit like [Langual](http://www.langual.org/langual_Thesaurus.asp) but we couldn’t use Langual as in local food system, not only food products are sold. People sell and buy soap, cosmetics, cleaning products, etc.

Also, IDs like GTIN doesn’t meet our need as a GTIN doesn’t tell the precise nature of a product, like the variety of an apple. Some webshops specialized in fruits might want to classify apples in different product categories depending on variety for instance, so GTIN is not enough.

So we choose the following “criteria” to uniquely identify products:

* First a **product type**, we are building a home made taxonomy that is more **“sales oriented”**. It tells if we talk about a carrot or a soap or a chili con carne or a camembert cheese.
* Then some **facets help identify more precisely** the products:
  * If the product has a unique **“living/mineral” source**, what is the source? For instance a steak has as source a living cow from a specific breed. If a product is composed it can be decomposed through the “transformation flow” mentioned above and each component can be described following the same process.
  * If the product has a unique “living/mineral” source, **what part or product of this source is used**? For instance honey comes from a unique living source which is a bee from a specific breed. The part of product of source concerned here is “honey”. If we talk about a carrot, the source will be the carrot variety, and the part concerned will be “the root”. If I talk about carrots seeds, the part concerned will be the seeds. If I sell carrots with the leaves it will be “whole plant”.
  * Every product sold will have gone through some sort of **processes**, at a minimum a tomato has been “harvested” from the living tomato plant. So even what we call “raw products” have undergone some basic process. Salt will have been “dried”, etc.
  * Each product has a **geographical origin**, it comes from somewhere. A cocoa bean can be from the same producer (big farmer owning lots of parcels for instance), go through the same harvesting, fermenting, drying processes, come from the same variety of cocoa plant, BUT come from a different location.
  * Products can have certifications/labels
  * Products can have some physical characteristics (soft, tender, etc.)
  * Products can have some specific claims (“gluten free”, “zero salt”, etc.)
  * And products can have a specific brand

For now we have treated physical characteristics, claims and brand as properties with only plain text content. We will probably evolve and treat them as glossaries as well in the future.

* And to finish a product is also identify with a **dimension and unit**, like potatoes are sold by 1 x kg, a jar of tomato sauce is sold by 1 x item, the item here being a “jar of 500 ml tomato sauce”.

## Modularization approach

For now we have only separated the business logic from the product nature logic. We want to evolve that and split the business logic to make the standard adoption easier, enable actors to adopt only one part or the other of the standard depending on their use case. Our aim is also to make the standard easier to maintain and evolve.

So we will probably go toward a standard architecture that could look like that:

![](https://lh3.googleusercontent.com/wGPQ7aCO6jWnLvdUOZDH_gLGEvKUReA0uMBKQDJDkZQ5xMgd-BTWp2srz2rbRg1Tb9Kh2vEUGqsjwwqAItg_PJfGkafAKCLcuvYgdQuhOQiMY0daaSHQQEPoXs4EY4kkNwblOAxh =624x345)

We need some more thinking with Bernard and the consortium members on that, and that will be part of the work for the next iterations.

We also want to build more on “bricks” that have already been built by other actors and can solve some of our issues. For instance the “agent” ontology have been much more refinely worked on by the Virtual Assembly for some other projects. Bernard has worked with Open Source Ecology on a much more refined measure ontology that we could also use instead of rebuilding it.

## Next steps

Our next step on the standard development are:

* test live this first stable version of the standard through the development of a “live prototype”
* modularize better and build the appropriate intersection models

Also we are still moving forward on structuring the consortium. We are at the moment writing the “games rules” for the Data Food Consortium community and will publish them soon, using the [#codesocial](http://codesocial.org/) methodology. We are applying for some grants as well at the moment to be able to start paying the job of the team working actively on this project.

So here is where we are at! Feel free to comment on GitHub and contact us on [hello@datafoodconsortium.org](mailto:hello@datafoodconsortium.org) :-)