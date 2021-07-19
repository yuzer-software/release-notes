# July 2021 - Version 1.7.0

- Contact stock reservations and orders are now displayed on it's contact page. You can enlarge the section as others by clicking on it's title.
- We improved some choices in cancellation modal that proposed _cancel_ to cancel the operation and _cancel_ to confirm the cancellation.
- We improved the performance of some screens including the accountancy documents list screens, and some elements of the basket screen.

## Payment means

### Associated to basket types

Payment means may be associated to a subset of basket types: when registering a payment, only the payment types associated to the corresponding basket type will be available.

## Entity configuration -- automatic mail processing

It's now possible to opt in to automatic mail processing. As this option requires your consent, it is not enabled by default and you need to set it on the mail entity configuration page.

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

- Workshop workload was not updated when switching date on the day view
- Date selection on the accountancy journal was broken.
