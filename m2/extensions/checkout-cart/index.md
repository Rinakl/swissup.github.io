---
layout: default
title: Checkout Cart
description: magento 2 checkout cart module documentation
keywords: checkout ajax cart, ajax cart magento 2, ajax cart at checkout page
category: Checkout Cart
---

# Checkout Cart

Checkout Cart extension brings cart functionality on checkout page. It allows
to change items quantity and remove items from cart on checkout page. Also with
this module you can move totals under cart items block in checkout cart summary section.

Extension is compatible with [Firecheckout](../firecheckout) and default Magento 2 checkout.

{% include gallery.html images=site.data.gallery.m2.checkout-cart.index class="scroll phone-up-1 tablet-up-3 photoswipe" %}

### Contents

1. [Installation](installation/)
2. [Changelog](changelog/)
3. [Settings](#settings)
4. [Known Issues](#known-issues)

## Settings

![Settings](/images/m2/checkout-cart/settings.png)

##### Enabled

Enable cart function on checkout page

##### Move Totals Under Product Details in Order Summary

Move totals block under product details in checkout order summary

## Known Issues

##### Shipping method depends from totals on default checkout

When you have shipping method which has `Minimum Order Amount` set in config,
you can face following problem on default checkout:

 -  you add few products to cart and totals amount is greater
 than configured `Minimum Order Amount`
 -  on checkout `Shipping` step you select shipping method
 -  on checkout `Payment` step you decrease quantity and order amount
 becomes smaller than configured `Minimum Order Amount`
 -  shipping method selected on `Shipping` step becomes unavailable
 and you can't place order

This issue only happens on default Magento 2 checkout.
There is no such problem with [Firecheckout](../firecheckout).

##### Minimum Order Amount

Extension is not compatible with `Minimum order amount` config in
`Stores > Configuration > SALES > Sales > Minimum Order Amount` because of bugs
in Magento 2.

##### Product Stock Options

Extension does not support `Maximum Qty Allowed in Shopping Cart`,
`Minimum Qty Allowed in Shopping Cart` and `Qty Increments` settings from
`Stores > Configuration > CATALOG > Inventory > Product Stock Options`.
