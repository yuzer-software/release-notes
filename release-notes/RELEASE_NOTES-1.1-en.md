# April 2021 - Version 1.1.7

We have fixed the ability to associate an Ordered or Pending order dealer file with a VIN when the VIN does not exists in the national registry or any of our connected manufacturers.

# April 2021 - 1 (Version 1.1.6)

Welcome to the April 2021 - 1 release of Yuzer.

This version includes a major rewrite of orders management from the basket to the reception. It aims to better reflect the actual status of baskets, customer reservations and supplier orders. It also aims to make all interactions easier and smoother while automating many operations for you.

## New logo

Yuzer has now a final logo and icon shipped with the application. We hope you will like it as much as we do!

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/icon.png" width="100"/>

# What's new

When launching the application with a new version we now open the What's new page so that you can immediatly understand our changes and benefits from the new features and improvements.

You can always see the What's new page again by clicking on the version on the bottom-left corner of the app.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/version-click.png" width="100%"/>

## New basket to reception workflow

This new version introduce a major rewrite of the stock and reservation management workflow. We now have fully separated the customer reservations and the supplier orders.

This allows more flexibility in their management and reception process, allowing also to cancel one of them without impacting the other, that has it's own flow. It makes it also easier to browser all customer reservations and all product orders with their different states.

### Basket stock support

From a basket point of view we automated the way reservation and stock finalization is performed and displayed.

#### Automatic reservation

Just before creating an order form or a repair order is created we now automatically perform a reservation or ordering of the elements of the basket.

- Every element that is in stock is _Reserved_ on the stock
- Every element that is not in stock _Ordered_ and we automatically create, in addition to the customer reservation a supplier order that is _waiting for order_.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/auto-reservation-fr.png" width="100%"/>

Note that you can also dispatch manually the stock from the stock pop-up window.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/manual-reservation-fr.png" width="100%"/>

Reservation button allows you to reserve a single billing group, or all the basket if using the modal bottom button.

#### Preparing a basket's stock

Preparing a basket is a brand new feature that allows to place some elements of the stock in a specific bucket dedicated to the basket. This allows to make sure that, in addition to having the product _reserved_ theorically for a customer, it is really prepared by placing it in a specific place.

Our recommandation is that you keep a specific location in your warehouses for prepared baskets and that you keep boxes where you can print the basket storage label on.

In order to prepare the basket stock you can go to the basket and click on the _stock_ button or directly from a task detail.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/basket-stock-btn.png" width="160"/>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/task-pick-btn.png" width="160"/>

From this modal you can click on the picking button for each line that you want to prepare, this will try to auto-select the best emplacement from which to take the item. In case the emplacement is not the one of your choice you can edit it or eventually add some more emplacement if you take items from multiple locations to fullfill the line quantity.

Once all picking is defined correctly just click on the _Prepare_ button to trigger the preparation. We will move the content in the right location of your stock.

Note that stock preparation is an optional step but can help you to manage your stock in a better way and make sure that your workshop will be efficient when starting to work.

#### Processing of the basket stock

Processing of the basket stock is the last step of the workflow and the one that will indeed decrement the stock content and mark the reservation as processed.

#### Viewing reservation state in basket

We have updated the icons and states on the basket edition view so that it reflects the new states of reservations, preparation processing and cancelations of orders on the basket.

### Customer reservations

In addition to the basket stock changes we added a better support for customer reservations. Under the main stock tab you will now find the customer reservations sub-tab that offers you two sub-views:

- Current: Where you can easily search the active reservations.
- Historical: Where you can browse your reservation history by month.

### Orders

While customer reservations displays the reservations and resvervations on orders that customers made to you, the _orders_ tab allows to manage and track the orders that you made to your suppliers. And provide 3 sub-views:

- Waiting for order: Where you will find all lines that are not yet ordered.
- Ordered products: Where you can browser seemlessly all lines that are in an order and neither received or canceled.
- Orders: Where you can browse the actual orders that you made to your suppliers and that basically group multiple product order lines.

#### Waiting for order

This tab is critical as, when ordering some products from a customer basket (during a reservation of a product that is not in stock for example)

### Receptions

Reception is now made simpler with a quick add on the desktop application that will automatically match the best-order(s) for the product as well as the customer reservations.

When displaying the catalog we now automatically filter

## Improvements of supplier selection

We have made it simpler to select suppliers in multiple places in the application. The selector now allows your to quickly filter the supplier that you are looking for.

<div class="d-flex justify-content-center">
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.1.0/new-supplier-select-fr.png" height="150"/>
</div>

We will replace supplier selection with the new selector in the upcomming versions.
