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

# That's fixed

- When dispatching cash desk closing without event and with a configuration that requires manual validation the state was left as _dispatched_ rather than _validated_ and could not be validated in the UI.
