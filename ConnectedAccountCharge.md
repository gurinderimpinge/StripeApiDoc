**Connected Account Payment Charge Api**
----
Description : This will charge Amount Connected Account.

* **URL**

   v1/stripe/ChargeConnectedAccount

* **Method:** 
    Post
	
* **Data Params** <br />

<pre>
{
  "amount": (int required), 
  "description": "(string required)",
  "currency": "(string required)",
  "stripeAccountId": "(string required)" 
}

</pre>   

* **Example:** <br/>

<pre>
 
{
  "amount": 100,
  "description": "Amount charged from Contractor",
  "currency": "usd",
  "stripeAccountId": "acct_1CptSYCzjgWBdSku" 
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
        "applicationId": "ca_D7qPWqAA8US9TVLXwbtn7yo8MPYbDVBp",
        "applicationFeeId": null,
        "balanceTransactionId": "txn_1CptdWJO26RVIZrdYMLzNE5Z",
        "captured": true,
        "created": 1532074010,
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
            "risk_level": "not_assessed",
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
            "url": "/v1/charges/py_1CptdWJO26RVIZrdlzhodHgo/refunds",
            "stripeResponse": null
        },
        "reviewId": null,
        "shipping": null,
        "source": {
            "type": 0,
            "account": {
                "object": "account",
                "businessLogoFileId": null,
                "business_name": null,
                "business_primary_color": null,
                "business_url": null,
                "charges_enabled": false,
                "country": null,
                "currencies_supported": null,
                "debit_negative_balances": false,
                "decline_charge_on": null,
                "default_currency": null,
                "details_submitted": false,
                "display_name": null,
                "email": null,
                "external_accounts": null,
                "legal_entity": null,
                "metadata": null,
                "product_description": null,
                "statement_descriptor": null,
                "support_email": null,
                "support_phone": null,
                "support_url": null,
                "timezone": null,
                "tos_acceptance": null,
                "type": null,
                "payouts_enabled": false,
                "payout_schedule": null,
                "payout_statement_descriptor": null,
                "verification": null,
                "keys": null,
                "id": "acct_1CptSYCzjgWBdSku",
                "stripeResponse": null
            },
            "bankAccount": null,
            "card": null,
            "deleted": null,
            "sourceObject": null,
            "id": "acct_1CptSYCzjgWBdSku",
            "stripeResponse": null
        },
        "sourceTransferId": "tr_1CptdVCzjgWBdSkuWnybzdbt",
        "statement_descriptor": null,
        "status": "succeeded",
        "transferId": null,
        "transfer_group": "1fa63ecb-86d4-4c3b-b401-d3ee91de3f93",
        "id": "py_1CptdWJO26RVIZrdlzhodHgo",
        "stripeResponse": {}
    },
    "token": null
}

</pre>

* **Error Response:**
    Code: 400 Bad Request	
<pre>
{ 
    "message": "Must provide source or customer."
}
</pre>


	

