# Mai 2021 - Version 1.4.0

- On the item detail page, a graph draws the purchase price of the product for each reception as well as its weighted average price (average cost of each product) and the average market price (unweighted average).
- Supplier selection when creating a new vehicle vehicle file or product has been improved.
- We can now select which customer address to use when editing a receipt-invoice.
- When creating a new vehicle trial appointment we now auto-generate the task label. You can still change it which will cancel auto-generation process.
- You can now send an email to a customer from it's detail page. This requires an email client to be defined on your operating system.
- Visibility of the button that allows to assign a reference to a product without one on a basket has an increased visibility.
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/basket-button.png" width="200" class="mx-2"/>
- On the _waiting for order_ screen, the configuration of the pinned columns are now kept when you return to the page.
- Added a button to refresh the list and the status of the _waiting for order_ lines.
- It is now possible to cancel a line of _product's order_. When you cancel a line, all unreceived quantities are marked as _canceled_. If necessary, you can edit the quantity from the detailed orders screen to put it back in _ordered_ status.
- Added a button to refresh the status of an order on the details screen.
- It is now possible to access the order, linked to the line, from the _Product's order_ view.
- When invoicing, administrators can now choose not to impact the stock for any basket type. To do this, simply click on the _Extended options_ button in the _Basket stock management_ window. Note that the possibility of ignoring the stock impact already exists for vehicle preparation baskets and remains available to entitled users.
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/admin-ignore-stock-impact.png" width="200" class="mx-2"/>
- Receipts now only display the first name followed by the first letter of the user's last name

## Calls and ringover integration

- We added tooltips to better understand the icons on a call activity.
- You can now comment on a call activity to provide a quick summary of the call.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/call-comment.png" width="300" class="mx-2"/>

- List of your last calls can now be accessed directly from the top navigation bar.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/missed-call-pill.png" width="300" class="mx-2"/>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/recent-call-list.png" width="300" class="mx-2"/>

## Top navigation bar review

We have changed the top navigation bar layout for more clarity and functional logic.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/navbar.png" width="100%"/>

## Stock tabs improvements

We have changed the order and default view of the stock tab for a better logic and more direct access to ordering capability.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.4.0/stock-tabs.png" width="100%"/>

## Bug fixes

- Fix printing a cash desk closing that was sometimes truncated.
- Fix the error message when invoice edition fails.
- Fix the selection of the visual identity when editing a receipt-invoice.
- Fix display bug with very long product references on a basket (they are now truncated).
- Prevent avatar letters to be displayed on 2 lines.
- Reorder rules were broken for products having some unusual references.
- Fix turnover widget that failed to show in a rare situation with invalid catalog data.
- Fix an issue that prevented starting a vehicle loan when the fuel level was not defined in the dealer file and not set on the start modal.
