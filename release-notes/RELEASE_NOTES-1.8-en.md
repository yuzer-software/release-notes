# July 2021 - Version 1.8.0

## Baskets

- You may now send a vehicle basket a to the workshop even if the vehicle doesn't have a VIN (for example because the vehicle is ordered).

## Client selection (tasks, basket, etc.)

- When selecting a client, its vehicles are now displayed.

- In some contexts, we need to select, among other things, both a client and one of its vehicle. Therefore, it's now possible to select the vehicle directly together with the client.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/select-user-modal.png"/>

## Configuration of default values for loans

- In the administration menu, you can now access a new tab allowing to set default configuration values for the different loan types.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/loans-config.png"/>

## Added preparation and maintenance costs in the computation of a vehicle's margin

When a preparation or maintenance cession is invoiced, the amount now impacts the vehicle's margin. The cession list is visible on the vehicle dealer file.
Note that cessions that are not invoiced are not taken into account and an alert icon is displayed instead of the amount.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/dealer-file-cessions.png"/>

Also, when editing a document on a vehicle sale, an alert message will be displayed if Yuzer detects that a cession related to the vehicle file has not been invoiced.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.8.0/billing-document-warning.png"/>
