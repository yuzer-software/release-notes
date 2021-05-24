# Mai 2021 - Version 1.4.0

- On the item detail page, a graph draws the purchase price of the product for each reception as well as its weighted average price (average cost of each product) and the average market price (unweighted average).
- Supplier selection when creating a new vehicle vehicle file or product has been improved.
- We can now select which customer address to use when editing a receipt-invoice.
- Visibility of the button that allows to assign a reference to a product without one on a basket has an increased visibility.
- When creating a new vehicle trial appointment we now auto-generate the task label. You can still change it which will cancel auto-generation process.
- You can now send an email to a customer from it's detail page. This requires an email client to be defined on your operating system.

## Calls and ringover integration

- We added tooltips to better understand the icons on a call activity.
- You can now comment on a call activity to provide a quick summary of the call.
- List of your last calls can now be accessed directly from the top navigation bar.

## Top navigation bar review

We have changed the top navigation bar layout for more clarity and functional logic.

## Stock tabs improvements

We have changed the order and default view of the stock tab for a better logic and more direct access to ordering capability.

## Bug fixes

- Fix printing a cash desk closing that was sometimes truncated.
- Fix the error message when invoice edition fails.
- Fix the selection of the visual identity when editing a receipt-invoice.
- Fix display bug with very long product references on a basket (they are now truncated).
- Prevent avatar letters to be displayed on 2 lines.
- Reorder rules were broken for products having some unusual references.
- Fix turnover widget that failed to show in a rare situation with invalid catalog data.
- Fix an issue that prevented starting a vehicle loan when the fuel level was not defined in the dealer file and not set on the start modal.

# Mai 2021 - Version 1.3.0

- You can now edit quantities from the basket stock and order management modal.
- It is now possible to cancel an order line in WAITING FOR ORDER state that you created manually.
- We have added a robot icon for lines that have been created by the order bot.
- Tasks list (reservations etc.) now displays filtered status correctly and allows to clear all status filter (to search on all states)
- We now display vehicles trials and lend from all states on the vehicle loan's page (under the customer tab)
- Accountancy Staging journal is now paginated by month
- Documents logo size has been increased

## Visual identity

You can now configure multiple visual identity through an image gallery on the entity.

<img src="./assets/release-notes/1.3.0/identity-cfg.png" width="100%" class="mb-3"/>

Theses visual identity can be used on document edition

<img src="./assets/release-notes/1.3.0/identity-select.png" width="300" class="mb-3"/>

So that your documents reflect the brand or identity you wish to use

<img src="./assets/release-notes/1.3.0/identity-document.png" width="300" class="mb-3"/>

## Ringover integration

This release introduce the connection of Yuzer with Ringover for telephony service. It will enable to keep track of the customer phone interactions in the contact page's activity as well as receiving direct notifications to quickly access a contact's page in app.

### Configuration

In order to setup ringover integration go to the Phone section of the administration panel and follow the steps.

<img src="./assets/release-notes/1.3.0/ringover-cfg.png" width="100%" class="mb-3"/>

Note that after login ringover will not redirect you to the correct location, so you may want to click once again on the step 1 link after login.

### Setup phone numbers

Once ringover is connected you must setup the phone numbers of your employees so that the notifications and calls are correctly associated.

<img src="./assets/release-notes/1.3.0/ringover-user.png" width="100%" class="mb-3"/>

### Call notification

When you receive a phone call on your line Yuzer will send you a notification so that you can quickly access the customer detail.

<img src="./assets/release-notes/1.3.0/ringover-notification.png" width="200" class="mb-3"/>

### Customer page activity

We also log the customer phone call activity directly on the contact page.

<img src="./assets/release-notes/1.3.0/ringover-activity.png" width="300" class="mb-3"/>

## Basket picking from mobile app

It's now possible to _prepare_ customer baskets from the mobile app. A product may be added to the basket as a new line at the same time it is picked.

### Basket access

There are three ways to access the basket.

- From the _Last desktop app works_ (side menu): baskets you worked on from the desktop app are now displayed in the mobile app, and conversely.

  <img src="./assets/release-notes/1.2.0/last-works.png" width="200" class="mb-3"/>

- From your tasks, with the basket icon in the lower left corner.

  <img src="./assets/release-notes/1.2.0/open-basket-from-task.png" width="200" class="mb-3"/>

- By scanning the QR-code of the basket stock management modal (click on the QR-code to increase its size).

  <img src="./assets/release-notes/1.2.0/open-basket-stock.png" height="50" class="mb-3"/>

  <img src="./assets/release-notes/1.2.0/open-basket-stock-qr-code.png" height="50" class="mb-3"/>

### Basket display

The mobile app basket display is leveraged and optimized for basket picking. The quantity of product to prepare and already prepared are displayed for each basket line.

  <img src="./assets/release-notes/1.2.0/basket-detail.png" width="200" class="mb-4"/>

### Basket picking

In order to add a product to the basket, four information are required :

- the product,
- the stock location from which it is picked,
- the picked quantity,
- the basket line for which the product was picked.

#### Picking any product

You may click on the <img src="./assets/release-notes/1.2.0/pick-button.png" height="20"/> button to pick any product, using either the _scanner_ or the _manual input_.

- When **the product** is set, only the corresponding basket lines remain visible.
- When both **the product** and **the storage location** are set, the _total_ product quantity to prepare for this basket is computed.

<table class="mb-4">
  <tr>
    <td>
      <img src="./assets/release-notes/1.2.0/basket-detail.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="./assets/release-notes/1.2.0/scan-item.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="./assets/release-notes/1.2.0/scan-location.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="./assets/release-notes/1.2.0/filtered-basket.png" width="200" class="mx-2"/>
    </td>
  </tr>
  <tr class="text-center">
    <td>
      Before any selection →
    </td>
    <td>
      → Product scanning →
    </td>
    <td>
      → Storage location scanning →
    </td>
    <td>
      → Lines are filtered
    </td>
  </tr>
</table>

You may then perform multiple actions:

- clicking on a _line's_ pick button (<img src="./assets/release-notes/1.2.0/pick-line-item.png" height="20"/>) prepares _this line_ (and only this line) with the quantity indicated on the button (here: 20). The remaining quantity to prepare is updated.

  <img src="./assets/release-notes/1.2.0/pick-line-item-lg.png" width="200" class="mb-3"/>

- clicking on a _task group's_ or _billing group's_ pick button (<img src="./assets/release-notes/1.2.0/pick-group.png" height="20"/>) creates a new line in the corresponding group with the quantity indicated in the button (here: 22) and immediately prepare the new line.

  <img src="./assets/release-notes/1.2.0/pick-group-lg.png" width="200" class="mb-3"/>

- clicking on the "Auto-spread" button (just below the quantity) spreads the quantity on all existing basket lines. If the total quantity to prepare exceed the total quantity to prepare for this basket, you will have to create yourself a new basket line just like described above.

  <img src="./assets/release-notes/1.2.0/auto-pick.png" width="200" class="mb-3"/>

As soon as the quantity is not zero, these actions are still available.

#### Picking a product for a specific basket line

When no product is set, you may click on a basket line's pick button <img src="./assets/release-notes/1.2.0/pick-line-no-item.png" height="20"/>: the product and the quantity of the line are used for the picking. You should then set the storage location. The manual input is proposed by default because it lists the storage locations of your warehouse that should contain the product.

  <img src="./assets/release-notes/1.2.0/pick-line-no-item-lg.png" width="200" class="mb-3"/>

Note: if you need to pick your product from multiple locations, you will have to manually **decrease the quantity** to fit the quantity you really picked from the selected location, then _prepare_ the line, and then repeat the operation with another storage location. (At last, you should have done one picking per storage location.)

Note: any other action is still possible.

# Mai 2021 - Version 1.2.0

- Product detail screen now displays the customer reservations and suppliers order.
- Improvement of loading of the waiting for order lines.
- And their sorting by creation date that was not applied when supplier filtering was activated.
- Un-sellection of all the waiting for order products is now fixed.
- You can now configure some automatic reorder rules.
- Fixed an issue that prevented to update company address and legal information configuration.
- Improvements of reception when a single reservation was added twice.
- Order export is now fixed when no configuration is defined.
- Reserve button of the basket stock management modal is now disabled once the stock has been processed.

# April 2021 - Version 1.1.7

We have fixed the ability to associate an Ordered or Pending order dealer file with a VIN when the VIN does not exists in the national registry or any of our connected manufacturers.

# April 2021 - 1 (Version 1.1.6)

Welcome to the April 2021 - 1 release of Yuzer.

This version includes a major rewrite of orders management from the basket to the reception. It aims to better reflect the actual status of baskets, customer reservations and supplier orders. It also aims to make all interactions easier and smoother while automating many operations for you.

## New logo

Yuzer has now a final logo and icon shipped with the application. We hope you will like it as much as we do!

<img src="./assets/release-notes/1.1.0/icon.png" width="100"/>

# What's new

When launching the application with a new version we now open the What's new page so that you can immediatly understand our changes and benefits from the new features and improvements.

You can always see the What's new page again by clicking on the version on the bottom-left corner of the app.

<img src="./assets/release-notes/1.1.0/version-click.png" width="100%"/>

## New basket to reception workflow

This new version introduce a major rewrite of the stock and reservation management workflow. We now have fully separated the customer reservations and the supplier orders.

This allows more flexibility in their management and reception process, allowing also to cancel one of them without impacting the other, that has it's own flow. It makes it also easier to browser all customer reservations and all product orders with their different states.

### Basket stock support

From a basket point of view we automated the way reservation and stock finalization is performed and displayed.

#### Automatic reservation

Just before creating an order form or a repair order is created we now automatically perform a reservation or ordering of the elements of the basket.

- Every element that is in stock is _Reserved_ on the stock
- Every element that is not in stock _Ordered_ and we automatically create, in addition to the customer reservation a supplier order that is _waiting for order_.

<img src="./assets/release-notes/1.1.0/auto-reservation-fr.png" width="100%"/>

Note that you can also dispatch manually the stock from the stock pop-up window.

<img src="./assets/release-notes/1.1.0/manual-reservation-fr.png" width="100%"/>

Reservation button allows you to reserve a single billing group, or all the basket if using the modal bottom button.

#### Preparing a basket's stock

Preparing a basket is a brand new feature that allows to place some elements of the stock in a specific bucket dedicated to the basket. This allows to make sure that, in addition to having the product _reserved_ theorically for a customer, it is really prepared by placing it in a specific place.

Our recommandation is that you keep a specific location in your warehouses for prepared baskets and that you keep boxes where you can print the basket storage label on.

In order to prepare the basket stock you can go to the basket and click on the _stock_ button or directly from a task detail.

<img src="./assets/release-notes/1.1.0/basket-stock-btn.png" width="160"/>
<img src="./assets/release-notes/1.1.0/task-pick-btn.png" width="160"/>

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
  <img src="./assets/release-notes/1.1.0/new-supplier-select-fr.png" height="150"/>
</div>

We will replace supplier selection with the new selector in the upcomming versions.
