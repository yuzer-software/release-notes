# July 2021 - Version 1.7.0

- Contact stock reservations and orders are now displayed on it's contact page. You can enlarge the section as others by clicking on it's title.
- We improved some choices in cancellation modal that proposed _cancel_ to cancel the operation and _cancel_ to confirm the cancellation.
- We improved the performance of some screens including the accountancy documents list screens, and some elements of the basket screen.
- The id number of the vehicle dealer file is no longer displayed in the product list of documents (invoice, order form, etc.).

## Deposits

In Accountancy -> Configuration, you can now configurate default deposit amounts for different kind of operations.

You can choose a fixed amount or or percentage with a rounding strategy.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/deposit-config.png"/>

## Payment means

### Associated to basket types

Payment means may be associated to a subset of basket types: when registering a payment, only the payment types associated to the corresponding basket type will be available.

### Associated to cashdesks

In Accountancy -> Configuration, cashdesks are now created and configured in a new tab.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/cashdesk-config.png"/>

The main evolution here is that you now have to associate means of payment to cashdesk in order to have more relevant choices during payments. You can only select one "cash" mean of payment per cashdesk.
<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/cashdesk-modal.gif" width="100%"/>

### Quick payments

In order to enhance the payment experience, the payment window has been tweaked. You can now automaticaly fill the amount field with a single click.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/cashdesk-modal.gif"/>

In case of a configured default deposit, you can choose the "deposit" section to automatically fill the fields with the deposit amount.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/payment-deposit-modal.gif"/>

As you can see, when choosing a cash payment type Yuzer now allows you to enter the amount received from the customer in addition to the desired payed amount and displays amount to give back to the customer.

## Repair order booking

We have added multiple improvements to the repair order booking in order to make the process smoother.

- In case you configured views in the workshop to split mechanics dedicated time between repairs and vehicle preparations, we automatically select the repair view.

Once the customer, vehicle and work defined (either through template or by specifying a detail and duration) you can select the workshop task place.

- In order to select it just click on the desired time on the calendar week view, or quickly access to the day view by selecting the day. This will allow you to quicly pre-assign the mechanic to assign or to have a better view on the time on which to place the appointment.

Once the workshop appointment is defined Yuzer automatically switch on the reception/delivery calendar so that you can define appointments with your customer.

You can then, if you wish add a courtesy loan.

Once all information are complete you can

- Either create the basket but not send it to the workshop; This will allow you to eventually fill-in details of the repair, split tasks and add products before you send it to the workshop.
- Either quickly create the basket and directly send it to the workshop.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/booking-modal.gif" width="100%"/>

## Correction de bugs

- Workshop workload was not updated when switching date on the day view.
- Date selection on the accountancy journal was broken.
- Vehicle load repayment cannot be reserved in stock anymore.

## Beta - Task creation on email

It's now possible to opt in to automatic mail processing. As this option requires your consent, it is not enabled by default and you need to set it on the mail entity configuration page.

<div class="alert alert-info">
This feature is released as Beta. It can be used right now and will be improved in next versions. Feel free to provide feedbacks.
</div>

<div class="alert alert-warning">
Warning, in beta, feature disable may take quite a while. If you activated then opt out of the feature please contact our support team if you whish Yuzer to stop fetching your emails.
</div>

Yuzer can now create automatically tasks based on some pre-formatted email reception.

To enable the feature please go to the email configuration to enable the feature by checking _Subscribe to automatic email analytics_.
Make sure that you entered your credentials again to save the configuration.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/emailfetch-setup.gif" width="100%"/>

Once enabled you must initialize the mailbox from the _Inbox_ tab. Once started it may take a while for Yuzer to fetch emails.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/emailfetch-init.gif" width="100%"/>

Last step is to configure templates for Yuzer to create tasks.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/emailfetch-setup.gif" width="100%"/>

You will then find tasks in the various list or calendar of the targetted workspace.

<img src="https://raw.githubusercontent.com/gear-group/release-notes/master/release-notes/1.7.0/emailfetch-task.png" width="100%"/>
>>>>>>> 08ac8ae... Add email beta feature to release notes.
