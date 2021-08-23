# July 2021 - Version 1.8.0

- Improvement of handling for some motorcycle registrations with A-00-A type of plates.
- You can now send a basket to the workshop with a vehicle type (no vin associated).
- You can now use the mouse wheel to change quantities.
- You can directly change tasks status from _to do_ to _done_ in tasks lists.
- File number is not printed anymore on the vehicle line in invoices.

## Baskets

- You may now send a vehicle basket a to the workshop even if the vehicle doesn't have a VIN (for example because the vehicle is ordered).

## Contact selection (tasks, basket, etc.)

- When selecting a contact, its vehicles are now displayed.
- In some contexts, we need to select, among other things, both a contact and one of its vehicle. Therefore, it's now possible to select the vehicle directly together with the contact.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/select-user-modal.png" width="100%"/>

## Loan documents completion

We added some more information to be displayed on the load document:

- Start date
- End date
- Maximum distance
- Daily fee
- Fuel fee

### Configuration of default values for loans

- In the administration menu, you can now access a new tab allowing to set default configuration values for the different loan types.

<div class="d-flex justify-content-center">
    <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loans-config.png" />
</div>

### Starting a loan

When you start a loan Yuzer pre-fills the added fields with the configured default values. You can of course adjust them specifically for your customer.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loan-start-modal.png" width="100%"/>

The informations are then added to the document.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loan-document.png" width="100%"/>

## Added preparation and maintenance costs in the computation of a vehicle's margin

When a preparation or maintenance cession is invoiced, the amount now impacts the vehicle's margin. The cession list is visible on the vehicle dealer file.
Note that cessions that are not invoiced are not taken into account and an alert icon is displayed instead of the amount.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/dealer-file-cessions.png" width="100%"/>

Also, when editing a document on a vehicle sale, an alert message will be displayed if Yuzer detects that a cession related to the vehicle file has not been invoiced.

<div class="d-flex justify-content-center">
  <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/billing-document-warning.png"/>
</div>

## New basket edition layout

Billing groups are now placed in tabs for better lisibility.

You can still drag and drop lines between groups. When multiple target groups exists you now have to pre-select the target group.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/basket-tabs-multi.gif" width="100%"/>

## Basket cancellation

When you cancel a basket, Yuzer now cancel automatically for you all customer reservations as well as reception/delivery/loan and workshop tasks.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/basket-cancel.gif" width="100%"/>

# That's fixed

- Yuzer did not prevent a user to generate two trade-in documents for the same vehicle from two different baskets.
- The term "Workforce" was not set in when a workforce line was added to the basket with no label.
- Various fixes when linking a vehicle dealer file to a basket.
