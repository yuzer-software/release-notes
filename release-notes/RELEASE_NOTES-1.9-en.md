# August 2021 - Version 1.9.0

## Product category changes

We have split the "other_services_and_taxes" into "other_services" and "other_taxes" in order to provide more VAT automation in the future. However, this process cannot be fully automated and requires your attention.

We have renamed the _other_services_and_taxes_ category to _other_services_ in all catalogs, but we didn't renamed it elsewhere, especially in accountancy mapping rules.

<div class="alert alert-danger">
  <ul>
    <li>
      Please do check your accountancy rules (Accountancy > Accounts configuration)<br/>
      <img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/accountancy-rule.png"/>
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

## Negative stock

In Stock -> Stock tab, there is now a new button "Negative Stock" that will lead to a new page displaying any products having a negative stock in at least one location.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/negative-stock.png" height="160"/>

## Overriding prices

It's possible to override vehicle's price, when it doesn't own to concession

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/override_prices.gif" height="160"/>

## Purchase invoice date

In the vehicle display, you can now find and modify the purchase invoice date.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.9.0/purchase-invoice-date.png" height="160"/>
