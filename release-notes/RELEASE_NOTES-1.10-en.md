# September 2021 - Version 1.10.0

- We improved products in stock filtering which should provide better results.

# Dashboard

The "Turnover" widget configuration has been clarified and has a new feature: filtering or grouping by basket type.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/turnover.png" height="320"/>

A new _Workforce_ widget has been added and allows to to display the **Invoiced** time or turnover of the workshop.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/workforce-widget.png" height="320"/>

# Calendar

You can now display multiple workspaces in a single calendar.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/multiple-workspaces.png" height="140"/>

When multiple workspaces are displayed:

- The load is displayed as unknown as it can only take the workshop tasks in account.
- Tasks colors uses the multiple workspaces configuration.

# Task creation when invoicing with pending cessions

When a basket is invoiced and some of the cessions (prepair / repair) have not been finalized, a task is automatically created in the commercial management calendar.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/incomplete-cession-warn.png" height="140"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/incomplete-cession-create.png" height="140"/>

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/incomplete-cession-task-cal" height="140"/>

# Trade-in estimation

In the event of a trade in, you can now fill some new fields to estimate the selling cost of the trade in vehicle and the cost of the repairs.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/trade-in-estimate.png"/>

These fields are optional by default but can be made mandatory by the admin in the _Commercial management tab_ (see below).

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/trade-in-estimate-mandatory.png"/>

If you defined a _recommended margin_ in the commercial management configuration (see below) the estimated sale price and repairs are used to compute a recommended purchase price.

# Commercial management

A new option "Commercial management" is now available in the "Settings" and will allow you to access these tabs:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/commercial_config.png"/>

We moved CGV and loan configuration here.

## Commercial management tab

You will also find a brand new menu that will allow you to access a new set of parameters:

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/commercial_config_tab.png"/>

### Default document validity duration

This new parameter allow you to define, in days, the default validity duration for commercial proposal documents in the application. The validity date will be automatically pre-filled when you'll generate a commercial proposal.

### Trade in estimate and recommended margin

If "yes" is selected the estimate sell price and repair cost are mandatory (see _Trade-in estimation_), if not are remain optional.
In addition you can configure an optional recommended margin that is used to compute the recommended purchase price on the trade in.

# Loyalty programs

You can now manage loyalty programs directly in Yuzer.

## Loyalty program configuration

Loyalty programs are defined in the "Administration" menu, section "Loyalty programs". You may define as many loyalty programs as you want. Here you can see two programs: Yuzer Premium and Yuzer Ultimate.

* Yuzer Premium gives to the subscriber 10% of immediate discount on all clothes and 5% of immediate discount on all Blackbird products supplied by Bihr.
* Yuzer Ultimate gives to the subscriber 20% on everything that may be discounted by a loyalty program.

Currently, we have some limitations: vehicles cannot be discounted by a loyalty program, as well as services under the "services and taxes" category (of course, taxes cannot be discounted).

Note that the brand must be the exact, case sensitive name of the brand. An empty brand matches all brands.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/loyalty-config.png"/>

## Subscribing to a loyalty program

You may register a contact loyalty program subscription from the contact page edition or directly from the basket. Below is how to:

* Add a subscription from a basket
* Add a loyalty membership to the billing group (Note that you cannot have more than one loyalty membership applied to a billing group). We will describe in Section "Apply contact's loyalty membership" the effect on the basket.
* Remove a loyalty membership from a billing group.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/loyalty-subscription.gif"/>

## Apply contact's loyalty membership

Below is the result of applying the "Yuzer Premium" loyalty program described above to a billing group containing tree lines. The applied loyalty program is displayed on the top of the billing group, and new billing group lines are added to summarize how the loyalty program impact the basket.

In fact, we have one line per VAT value. In our example, all discounted lines have 20% VAT value so we only have one line of loyalty discount. This line has a total TTC that sums all discount applied and contains the description of each discounts:

* BIH-0040038 is neither a garment, neither a Blackbird product so no discount is applied.
* BIH-01-142 is a garment: it matches the first rule of the program and thus this rule applies, resulting in a 10% discount.
* BIH-1003038 is not a garment but a blackbird product provided by Bihr so the second rule applies, resulting in a 5% discount.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.10.0/loyalty-basket.png"/>

# That's fixed

- When dispatching cash desk closing without event and with a configuration that requires manual validation the state was left as _dispatched_ rather than _validated_ and could not be validated in the UI.
- It is possible to take negative payments (refund).
