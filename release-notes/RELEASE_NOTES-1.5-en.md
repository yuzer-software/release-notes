# June 2021 - Version 1.5.0

- Yuzer mobile application is now available on the App Store for iOS and Play Store for Android.
- We have improved the synchronization between the basket and the vehicle file when a vehicle has been updated. Also it is now also possible to force the update from the context menu of the vehicle in the basket.
  <img src="https://raw.githubusercontent.com/yuzer-software/release-notes/master/release-notes/1.5.0/sync-basket-dealer-file.png" width="200" class="mx-2"/>
- We now display weighted average purchase price for stock value. In previous versions we used FIFO based stock value which is less efficient for some scenarios (like finding an missing item in an inventory).
- We added a shortcut to create a new vehicle sale from the top navbar.
- Spellchecker suggestions can now be applied through a right click.
- Vehicle stock lisibilité has been improved.

## Update of the automatic reservation algorithm

When a product must be ordered because there is not enough stock, the algorithm will try to reserve among the _Reserved order_ quantity first before reserving in the physical stock.

> For example:
>
> Let us suppose that a customer wants to buy 3 units of a product with only 2 left in stock.
> Let us also suppose that this product has the following re-order rule: "at least 1 in stock and must be ordered per sets of 2".
>
> When reserving the basket,
> Before: the algorithm would have created 2 units in _Waiting for order_ and saves 2 _Reserved_ in stock and 1 _Reserved order_ for the basket.
> Now: the algorithm still creates 2 units in _Waiting for order_ but now saves 1 _Reserved_ in stock and 2 _Reserved order_ for the basket.
>
> If we change the rule with: "at least 2 in stock and must be ordered in sets of 2".
> Before: the algorithm would have created 4 units in _Waiting for order_ to fulfil minimum of 2 in stock and saves 2 _Reserved_ in stock and 1 _Reserved order_ for the basket.
> Now: the algorithm still creates 4 units in _Waiting for order_ to comply with the rule but now saves 0 _Reserved_ in stock and 3 _Reserved order_ for the basket.
>
> And finally if the product does not have a re-order rule, there is no change.
> The algorithm creates 1 units in _Pending order_ and saves 2 _Reserved_ in stock and 1 _Reserved on order_ for the basket.

Note that it is still possible to force the quantity to reserve for a basket line.

## Bug fixes

- Fixes an issue preventing a receipt from being closed with a line to prepare 2 different lines on a basket for the same product.
- Updating a contact could loose the link to it's document gallery. This is now fixed.
- Fix an accountancy issue when a quantity had a huge quantity of decimals (0.333333333 for example)
