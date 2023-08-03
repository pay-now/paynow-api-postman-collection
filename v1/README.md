# About 

This is a simple Postman collection for Paynow API version 1.
Collection allows you to create a basic requests in Paynow Sandbox environment.

# How to use

## Preparing the environment

1. Download collection for Paynow API `paynow.postman.collection.json` and environment variables `paynow.sandbox.postman.environment.json`.
2. Import them into your Postman application.
3. Select `Paynow Sandbox` environment

## Creating requests

To see the full documentation of our API please refer to the following website: https://docs.paynow.pl

Make a payment:

1. Send `Payment request`.
2. Open returned URL in your web browser and authorize a payment.
3. Send `Payment status`, to retrieve current payment status

Make a payment [WHITELABEL]:

1. Send `Payment request [WHITELABEL]`. Should return paymentId with PENDING status
2. Send `Payment status [WHITELABEL]`, to retrieve current payment status. Should be updated to `CONFIRMED` after some time.

Make a refund:

1. Send `Payment request`.
2. Open returned URL in your web browser and authorize a payment.
3. Send `Payment status`, to retrieve current payment status
4. Send `Payment refund`
5. Send `Payment status`, to retrieve current refund status