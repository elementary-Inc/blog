---
title: The New elementary Store is Here
description: Stand-alone, open source, and much more flexible
author: cassidyjames
tags:
  - meta
---

For the past several months our web team has been working on a new merch store to replace the old manual front-end—and we're ready to debut that work for you all now. Say hello to the new [store.elementary.io][store]!

<div style="text-align: center" markdown="1">
[Visit the Store][store]{: .button }
</div>

We've long offered a simple store as a way to get official branded merch while directly supporting development of elementary OS. We've partnered with [Printful](https://printful.com) for years thanks to their excellent quality products, but our previous store page was a very finicky PHP app that required manual uploading of print files and fiddling with product JSON—basically, unfriendly to both developers and designers. As a result, we only ever offered a small selection of products and were largely unable to spend the time to design and upload new ones.

Printful does offer a number of integrations with popular selling platforms like Shopify and Etsy, but they weren't a good price fit for the relatively low volume plus global reach of our store, nor were they able to be as integrated into our existing website and design style as we'd like.

Instead, we've built an open source front-end for Printful stores, leaning on their [store API](https://www.printful.com/docs) and [Stripe Checkout](https://stripe.com/payments/checkout). We use the Printful dashboard to create and manage products, then the front-end automatically pulls in the changes from the API. Customers can browse and add products (including different sizes, colors, and other variants) to their cart, then check out using the straightforward and secure Stripe Checkout. The result is a simple and modern feeling store front-end that doesn't require any duplication of work or manual syncing of products—all while enabling us to rapidly try out new products and variants with very low overhead.

Using Stripe Checkout also enables us to easily support nice features like Google Pay, saving and reusing payment info securely stored with Stripe, and coupon codes—in fact, as a thanks for reading the blog, we're offering the first 100 people a coupon for 10% off their first purchase: just enter `BLOG10` at checkout!

<div style="text-align: center" markdown="1">
[Visit the Store][store]{: .button }
</div>

Like everything we do at elementary, we've released this Printful store front-end as [an open source project on GitHub][repo]. We encourage people to file issues and pull requests for improvements, and we hope it can serve as a useful base for others to build their own low maintenance, on-demand merch store. This work was largely lead and developed by [Blake Kostner](https://github.com/btkostner), with design and front-end support from me, and product/logistics support from [Liz Kecso](https://github.com/ekecso).

If there's a specific type of product or design you don't see that you'd like us to offer, be sure to [file an issue][repo] or mention us on social media, and we'll see what we can do.

[store]: https://store.elementary.io
[repo]: https://github.com/elementary/store
