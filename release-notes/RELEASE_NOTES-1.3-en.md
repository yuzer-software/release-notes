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

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.3.0/identity-cfg.png" width="100%" class="mb-3"/>

Theses visual identity can be used on document edition

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.3.0/identity-select.png" width="300" class="mb-3"/>

So that your documents reflect the brand or identity you wish to use

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.3.0/identity-document.png" width="300" class="mb-3"/>

## Ringover integration

This release introduce the connection of Yuzer with Ringover for telephony service. It will enable to keep track of the customer phone interactions in the contact page's activity as well as receiving direct notifications to quickly access a contact's page in app.

### Configuration

In order to setup ringover integration go to the Phone section of the administration panel and follow the steps.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.3.0/ringover-cfg.png" width="100%" class="mb-3"/>

Note that after login ringover will not redirect you to the correct location, so you may want to click once again on the step 1 link after login.

### Setup phone numbers

Once ringover is connected you must setup the phone numbers of your employees so that the notifications and calls are correctly associated.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.3.0/ringover-user.png" width="100%" class="mb-3"/>

### Call notification

When you receive a phone call on your line Yuzer will send you a notification so that you can quickly access the customer detail.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.3.0/ringover-notification.png" width="200" class="mb-3"/>

### Customer page activity

We also log the customer phone call activity directly on the contact page.

<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.3.0/ringover-activity.png" width="300" class="mb-3"/>

## Basket picking from mobile app

It's now possible to _prepare_ customer baskets from the mobile app. A product may be added to the basket as a new line at the same time it is picked.

### Basket access

There are three ways to access the basket.

- From the _Last desktop app works_ (side menu): baskets you worked on from the desktop app are now displayed in the mobile app, and conversely.

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/last-works.png" width="200" class="mb-3"/>

- From your tasks, with the basket icon in the lower left corner.

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/open-basket-from-task.png" width="200" class="mb-3"/>

- By scanning the QR-code of the basket stock management modal (click on the QR-code to increase its size).

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/open-basket-stock.png" height="50" class="mb-3"/>

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/open-basket-stock-qr-code.png" height="50" class="mb-3"/>

### Basket display

The mobile app basket display is leveraged and optimized for basket picking. The quantity of product to prepare and already prepared are displayed for each basket line.

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/basket-detail.png" width="200" class="mb-4"/>

### Basket picking

In order to add a product to the basket, four information are required :

- the product,
- the stock location from which it is picked,
- the picked quantity,
- the basket line for which the product was picked.

#### Picking any product

You may click on the <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/pick-button.png" height="20"/> button to pick any product, using either the _scanner_ or the _manual input_.

- When **the product** is set, only the corresponding basket lines remain visible.
- When both **the product** and **the storage location** are set, the _total_ product quantity to prepare for this basket is computed.

<table class="mb-4">
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/basket-detail.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/scan-item.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/scan-location.png" width="200" class="mx-2"/>
    </td>
    <td>
      <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/filtered-basket.png" width="200" class="mx-2"/>
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

- clicking on a _line's_ pick button (<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/pick-line-item.png" height="20"/>) prepares _this line_ (and only this line) with the quantity indicated on the button (here: 20). The remaining quantity to prepare is updated.

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/pick-line-item-lg.png" width="200" class="mb-3"/>

- clicking on a _task group's_ or _billing group's_ pick button (<img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/pick-group.png" height="20"/>) creates a new line in the corresponding group with the quantity indicated in the button (here: 22) and immediately prepare the new line.

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/pick-group-lg.png" width="200" class="mb-3"/>

- clicking on the "Auto-spread" button (just below the quantity) spreads the quantity on all existing basket lines. If the total quantity to prepare exceed the total quantity to prepare for this basket, you will have to create yourself a new basket line just like described above.

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/auto-pick.png" width="200" class="mb-3"/>

As soon as the quantity is not zero, these actions are still available.

#### Picking a product for a specific basket line

When no product is set, you may click on a basket line's pick button <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/pick-line-no-item.png" height="20"/>: the product and the quantity of the line are used for the picking. You should then set the storage location. The manual input is proposed by default because it lists the storage locations of your warehouse that should contain the product.

  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.2.0/pick-line-no-item-lg.png" width="200" class="mb-3"/>

Note: if you need to pick your product from multiple locations, you will have to manually **decrease the quantity** to fit the quantity you really picked from the selected location, then _prepare_ the line, and then repeat the operation with another storage location. (At last, you should have done one picking per storage location.)

Note: any other action is still possible.
