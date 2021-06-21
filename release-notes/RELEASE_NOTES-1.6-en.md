# June 2021 - Version 1.6.0

- Possibility to update the label of a product in a basket.
- The margin rate is now displayed in the _Summary_ box of the vehicle sales basket when the filter to display purchase prices and margins is deactivated.
- You can now filter on supplier on the _Product's order_ page.
- We added a page break on generated pdf documents to split the terms and conditions so that you can easely skip printing them if you wish not to.
- Accountancy journal page has a faster rendering when many lines are loaded.
- Products added to a reception are now added to the filtered location if one is specified and when not linked to a customer (they are still associated with the customer's basket if so).
- You can now filter baskets by closing dates. A basket is considered closed if it is invoiced and its balance is nil or if it is canceled.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/baskets-filtering-closed-date.png" width="400" class="mx-2"/>

- Contact activities now displays the author; we also improved icons on the list.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/contact-activities.png" width="400" class="mx-2"/>

- You can now easely add products to re-order from the _Waiting for order_ page.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/waiting-order-quick-add.png" width="100%"/>

## Avoiding contact duplications

When you create a new contact, we now automatically search for potential duplicates so that you avoid creating a duplicate when not needed.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/contact-duplicates.png" width="100%"/>

We use multiple fields of the contacts to find then so you should not create duplicates again.

If the contact you search is in the potential duplicates list just click on him to access it's contact page.

## Accountancy auto-validation and export

We added options to enable auto-validation of invoices, trade-in and cessions in accountancy.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/accountancy-auto-validation.png" width="200" class="mx-2"/>

If the options are enabled, then we automatically process an edited document to create lines in the pending journal.
If automatic pending writings is enalbed then the lines are writen directly to the journal. In case of an error (wrong account mapping etc.) writings are still writen in the pending journal rather than the journal so that you can fix the issue.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/accountancy-to-validate.png" width="100%"/>

You also can configure a daily export of the journal to your own FTPS server.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/accountancy-ftp-config.png" width="200" class="mx-2"/>
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.6.0/accountancy-to-validate.png" width="200" class="mx-2"/>

The file will be generated every night with the content of journal lines written since the last export.

## New features on repcetions

### Re-opening

It is now possible to re-open a closed reception to add new lines.
The processed lines cannot be modified.

### Annulation

Canceling a reception is now possible. You can choose to cancel only a few lines or all lines of a reception.

<img src="next-version/reception-new-menu.png" width="320"/>

A canceled line is displayed with grayed out text with the <img src="next-version/reception-ban-icon.png" width="16" /> icon, as below.

<img src="next-version/reception-canceled-line.png" width="1024"/>

When canceling, the following different actions are performed for each of the lines to try to return to the state before closing:

- Cancellation of the stock quantities on the reception storage location
- Cancellation of stock prices for the product (FIFO price, average price)
- If existing, cancellation of the associated order line
- If existing, cancellation of the reservation / preparation for a customer

The storage locations specified on reception may have been updated between the closing and the cancellation.
If the quantity is too low (_quantity of the storage location < quantity received_), a window open asking you to resolve and specify the storage locations to be impacted for the cancellation.

The following image shows the validation window.

<img src="next-version/reception-cancellation-modal-1.png" width="1024"/>

We find that a line had been closed with 4 quantities received, all stored at the storage location: _Showroom/Étagère 1/ Planche 1/ Paquet 1_.
However, it contains only 2 units of the product.

For the example, we choose to add the cancellation of 2 quantities on the _Emplacement inconnu_ (unknown location).

<img src="next-version/reception-cancellation-modal-2.png" width="1024"/>

Note that the number of items and the total price including discounts are computed ignoring the canceled lines.

<img src="next-version/reception-infos.png" width="384"/>

### Lines filtering

Filters have been added to be able to hide processed and canceled lines.
This should facilitate readability in particular when modifying a relatively large reception which have been re-opened.

<img src="next-version/reception-new-filters.png" width="896"/>

## Correction de bugs

- We removed the grouping on _Product's order_ that prevented the creating date sort to work correctly.
- Fix tab navigation under the stock tab
