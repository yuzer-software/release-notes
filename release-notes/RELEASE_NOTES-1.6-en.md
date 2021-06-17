# June 2021 - Version 1.6.0

- Possibility to update the label of a product in a basket.
- The margin rate is now displayed in the _Summary_ box of the vehicle sales basket when the filter to display purchase prices and margins is deactivated.

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

### Filtrage des lignes

Filters have been added to be able to hide processed and canceled lines.
This should facilitate readability in particular when modifying a relatively large reception which have been re-opened.
<img src="next-version/reception-new-filters.png" width="896"/>
