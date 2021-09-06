# August 2021 - Version 1.9.0

- When taking a new appointment through the quick workshop appointment feature the title of the created basket is now the one of the selected template, or, when you edit a custom description the first line of the description.
- The model name of a vehicle is now editable.
- It is now possible to generate an export with the products in stock into a **csv**, **excel** or **txt** file.
- It is now possible to convert balance into credit event if it creates a negative balance.
- An administrator can now choose to ignore to impact the stock of products for all types of basket while invoicing (initially only possible for baskets of _vehicle preparation_ type).
- It is now possible to collect a payment with an amount greater than the basket one.

## Product category changes

We have split the "other_services_and_taxes" into "other_services" and "other_taxes" in order to provide more VAT automation in the future. However, this process cannot be fully automated and requires your attention.

We have renamed the _other_services_and_taxes_ category to _other_services_ in all catalogs, but we didn't renamed it elsewhere, especially in accountancy mapping rules.

<div class="alert alert-danger">
  <ul>
    <li>
      Please do check your accountancy rules (Accountancy > Accounts configuration)<br/>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/accountancy-rule.png" width="100%"/>
    </li>
    <li>Please do check product categories in existing opened baskets</li>
    <li>
      Please do check that products now in the "other_services" category should not be in "other_taxes" (you may use the category filter as below)<br/>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/search-for-other-services.png" height="160"/>
    </li>
  </ul>
</div>

## Contacts

### Vehicle registration numbers

- The registration number of the vehicles of a contact are now displayed.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/vehicle-registration.png" height="140"/>

### VAT Exonerated

When creating or updating a client, you can now check "VAT exonerated" if you have a role among "ACCOUNTANT"
, "ADMIN" or "SALES_MANAGER".
A client with VTA exonerated will have his VAT set to 0% by default when adding items to a basket.

Note that the creation of a template from a basket belonging to a contact who is exonerated from VAT has been temporarily disabled.
Indeed, when we create a basket template, we currently save the price of the products as it was set on the source basket. Therefore, when the template is reapplied on a new basket, it is possible that the prices are without VAT. We plan to review the feature to avoid this kind of problem in the future.

## Negative stock

In Stock -> Stock tab, there is now a new button "Negative Stock" that will lead to a new page displaying any products having a negative stock in at least one of its location. Note that you can print the displayed page with the list of products.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/negative-stock.png" height="160"/>

## Overriding catalog vehicle prices

It is now possible to override the price of a vehicle in the catalog, even when the catalog is not managed by the dealership.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/override_prices.gif" height="160"/>

## Reserved vehicle filter

It is now possible to filter reserved vehicles.

<img src="./1.9.0/dealer-file-reserved-filter.png" width="475"/>

## Purchase invoice date

In the vehicle display, you can now find and modify the purchase invoice date.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/purchase-invoice-date.png" height="160"/>

## Reception printing

You can now use the print button on a closed reception to print the list.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/reception-print.png" width="100%"/>

## Product or vehicle lists access

We improved the navigation on vehicle and products lists; you can now click anywhere on the line to access the detail. Note that you can still select a text (reference, description) by double clicking on it or by dragging the mouse pointer to select a part of the text.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/line-select.gif" width="100%"/>

## Top search improvements

Global search has been improved for more comfort. Search is now performed on

- Dealer files
- Contacts
- Products

User experience has also been improved:

- The best-matching result is now displayed on top of the list and is pre-selected; it can be immediately accessed by pressing the _enter_ key.
- Navigation in results is enabled by using the arrow keys of your keyboard (selection is done by pressing the _enter_ key).
- You can access the the search screen of dealer files/contacts/products including the current search by using the _Advanced search_ option.

Please note that searching a vehicle in supplier systems or by registration is enabled only with a minimum of 6 characters but:

- Triumph is the only manufacturer that currently enables searching a VIN with the last 6 characters.
- A registration or VIN for other manufacturers must be entered completely.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/top-search.gif" width="100%"/>

## Renaming of label 'Waiting for delivery'

- Label 'Waiting for delivery' was renamed by the label 'Waiting for supplier' respectively in calendar view, with 'kanban' selected and in task edition.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/kanban_en.png" width="100%"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/status_en.png" width="100%"/>

## Tasks colors configuration

Default tasks colors can now be customized to fit your need. It can be configured entity/company wide (and will use the parent entity configuration if none is defined on a child entity) or overridden per user.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/task-color-config.gif" width="100%"/>

Note that each user can have their own color configuration. It can be set from _Account information > Workspaces_

# That's fixed

- Fixed a focus issue when editing the label of a basket line.
- Fixed an issue when one duplicates a rule on the account configuration.
- Fixed search filter of product categories not always returning the right results.
- Fixed an error when creating a billing group when there is none in the basket.
- Added a missing translation for the error message of editing a cession document with discounts.
- Various fixes when deleting or canceling a billing group.
- The VAT is now correctly updated when moving a non-stockable product into or out of a cession group.
- Fixed indefinitely pending page when trying to edit a purchase from a vehicle dealer file.
- Cannot add line to a basket converted from Repair Order to PGNA with a canceled workshop task.
- Drag and drop issues inside a sub-group and between billing groups have been solved.
- Display of stock status on a new basket line has been fixed.

Note: _Most fixes where included in 1.8.3 and 1.8.4 releases_

# Mobile application

- Some barcodes are prefixed or suffixed by spaces. These spaces are now automatically removed.
- Tasks are colorized as in the desktop application.
- After reception or transfer creation, the application automatically navigates to the add products page.
- When opening an empty reception or transfer, the application automatically navigates to the add products page.
- When a vehicle type is updated, the catalog search list is now refreshed to display an up-to-date result.
- Fixed a refresh issue with the basket cancellation window.
- Fixed the _total_ and _account_ buttons in the payment window that were not displayed for the PG&A and O.R baskets.
