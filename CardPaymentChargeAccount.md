**Card Payment Charge Api**
----
Description : This will charge Amount through Card.

* **URL**

   v1/stripe/CardPaymentCharge

* **Method:** 
    Post
	
* **Data Params** <br />

<pre>
{
  "amount": (int required), 
  "description": "(string required)",
  "currency": "(string required)",
  "CardToken": "(string required)" 
}

</pre>   

* **Example:** <br/>

<pre>
 
 {
  "amount": 100,
  "description": "Amount charged via card sample",
  "currency": "usd",
  "CardToken": "tok_1CpYQPwewrewVIZrdM29OTEOL"

}


* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Amount of usd 100 has been charged.",
    "error": null,
    "data": {
        "object": "charge",
        "amount": 100,
        "amount_refunded": 0,
        "applicationId": null,
        "applicationFeeId": null,
        "balanceTransactionId": "txn_1CpYjbJdghdgfhdgfhdgfh1AGPV6",
        "captured": true,
        "created": 1531993663,
        "currency": "usd",
        "customerId": null,
        "description": "Amount charged from Contractor",
        "destinationId": null,
        "disputeId": null,
        "failure_code": null,
        "failure_message": null,
        "fraud_details": {},
        "invoiceId": null,
        "livemode": false,
        "metadata": {},
        "onBehalfOfId": null,
        "orderId": null,
        "outcome": {
            "network_status": "approved_by_network",
            "reason": null,
            "risk_level": "normal",
            "rule": null,
            "seller_message": "Payment complete.",
            "type": "authorized",
            "id": null,
            "stripeResponse": null
        },
        "paid": true,
        "receipt_email": null,
        "receipt_number": null,
        "refunded": false,
        "refunds": {
            "object": "list",
            "data": [],
            "has_more": false,
            "total_count": 0,
            "url": "/v1/charges/ch_1CpYjbJO26RVIZrdnV6Dj3TL/refunds",
            "stripeResponse": null
        },
        "reviewId": null,
        "shipping": null,
        "source": {
            "type": 2,
            "account": null,
            "bankAccount": null,
            "card": {
                "object": "card",
                "accountId": null,
                "address_city": null,
                "address_country": null,
                "address_line1": null,
                "address_line1_check": null,
                "address_line2": null,
                "address_state": null,
                "address_zip": null,
                "address_zip_check": null,
                "available_payout_methods": null,
                "brand": "Visa",
                "country": "US",
                "currency": null,
                "customerId": null,
                "cvc_check": "pass",
                "default_for_currency": false,
                "dynamic_last4": null,
                "exp_month": 12,
                "exp_year": 2022,
                "fingerprint": "iNKOTdO5hDHKRzme",
                "funding": "credit",
                "last4": "4242",
                "metadata": {},
                "name": "Test Name",
                "recipientId": null,
                "three_d_secure": null,
                "tokenization_method": null,
                "description": null,
                "iin": null,
                "issuer": null,
                "id": "card_1CpYjKJO26RVIZrdp92I5PAQ",
                "stripeResponse": null
            },
            "deleted": null,
            "sourceObject": null,
            "id": "card_1CpYjKJO26RVIZrdp92I5PAQ",
            "stripeResponse": null
        },
        "sourceTransferId": null,
        "statement_descriptor": null,
        "status": "succeeded",
        "transferId": null,
        "transfer_group": "08f056b0-99f2-4ea4-9f48-94e9732662b4",
        "id": "ch_1CpYjbJO26RVIZrdnV6Dj3TL",
        "stripeResponse": {}
    },
    "token": null
}
</pre>


* **Error Response:**

    Code: 400 Bad Request
	
<pre>
{
  "message": "No such token: tok_1CpYQrtretetdM29OTEOL"
}
</pre>
 **Create Account  ApiDoc:** <br/>
[CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/edit/master/CreateAccount.md)<br/>

**Verify Account  ApiDoc:** <br/>
[Verify Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContractorAccount.md)<br/>

 **Contractor ApiDoc:** <br/>
[Charge PaymentFrom ContractorAccount Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ChargeAmountContractorAccount.md)<br/>

 **PaymentStatus ApiDoc:** <br/>
[PaymentStatus Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/PaymentStatusContractorAccount.md)<br/>

**Contractee ApiDoc:** <br/>
[Transfer PaymentTo Contractee Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/TransferPaymentToContractee.md)<br/>

**Cards ApiDoc:** <br/>
[CardToken  ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/CardPaymentToken.md)<br/>
[CardPaymentCharge  ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/CardPaymentChargeAccount.md)

	

