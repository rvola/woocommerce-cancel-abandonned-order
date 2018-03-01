# WooCommerce Cancel Abandoned Order 
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/rvola)

Cancel "on hold" orders after a certain number of days.

![banner](/.github/banner.jpg)

## Description

**WooCommerce Cancel Abandoned Order** allows you to add a small option that will take care of dealing with "abandoned" commands.

If you have check or transfer type orders for example, you will be able to set a maximum number of days to receive the payment.

WooCommerce Cancel Abandoned Order, will take care of checking this and change the status of the order to "Cancel" if you have not received payment on time.

Since version **1.3.0** the system takes care of returning your products abandoned orders in stock ... Amazing!


## Installation

This section describes how to install the plugin and get it working.

1. Upload the plugin files to the `/wp-content/plugins/woo-cancel-abandoned-order` directory, or install the plugin through the WordPress plugins screen directly.
2. Activate the plugin through the 'Plugins' screen in WordPress
3. By default you can control the orders on the payment gateways: Check and BACS. Go to the options of the payment pages on WooCommerce.

*To add another payment gateway, simply use the `woo_cao_gateways` filters, more information on the [Wiki](https://github.com/rvola/woo-cancel-abandoned-order/wiki)*

## Requirement

* PHP minimal: **5.3**
* WordPress minimal: **4.0**
* WooCommerce minimal : **2.2.0**

## Hooks
_Action_
* `woo_cao_cancel_order` ($order_id) / After cancel order.
* `woo_cao_restock_item` ($product_id, $old_stock, $new_stock, $order, $product ) / After restock product.

_Filters_
* `woo_cao_gateways` / Adds a payment gateway for the control.
* `woo_cao_default_days` / Default value of the number of days for order processing.

## Wiki
* [A help section on the code is available here](https://github.com/rvola/woo-cancel-abandoned-order/wiki)

## Frequently Asked Questions

#### What does the plugin do?

Depending on the options on the payment gateway options page *(enabled or disabled, maximum number of days)*, the plugin will fetch every day at midnight, the "on hold" commands with the payment gateway type *(default Check, BACS)* and if the maximum number of days indicated and exceeded, the system will take care to update the status of the order.

#### Restock

If you checked the box to enable this feature in the gateway, the system will restock each product line of the abandoned order.

## Links

* [**Changelog**](https://github.com/rvola/woo-cancel-abandoned-order/blob/master/CHANGELOG.md)
* [**Download on WordPress**](https://wordpress.org/plugins/woo-cancel-abandoned-order/)
