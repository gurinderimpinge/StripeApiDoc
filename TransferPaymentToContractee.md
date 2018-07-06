**Transfer Payment to Contractee Account Api**
----
Description : This will Transfer Payment from Contractor Account to contractee account.

* **URL**

   v1/stripe/TransferPayment

* **Method:** 
    Post
	
* **Data Params** <br />

<pre>
{
    "transferToAccount": "(string required)",
    "amount": "(string required)",
    "tranferGroup": "(string required)",
    "paymentDescription": "(string required)",
    "currency": "(string required)",
    "stripeCustomerId": "(string required)",
    "receiptEmail": "(string required)",
}	 
</pre>   

* **Example:** <br/>

<pre>

{
    "transferToAccount": "acct_1CkrOiIS8FLYKBGJ",
    "amount": "150",
    "tranferGroup": "bee8d641-e25c-4177-8b94-0e01450098d9",
    "paymentDescription": "Payment transfer to contractor",
    "currency": "usd",
    "stripeCustomerId": "py_1CkoVfJO26RVIZrd9esDbTrp",
    "receiptEmail": "test@gmail.com"
}

* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": null,
    "error": null,
    "data": {
        "object": "transfer",
        "amount": 142,
        "amount_reversed": 0,
        "balanceTransactionId": "txn_1CkrRgJO26RVIZrd0lmafcGq",
        "created": 1530873948,
        "currency": "usd",
        "destinationId": "acct_1CkrOiIS8FLYKBGJ",
        "destinationPaymentId": "py_1CkrRgIS8FLYKBGJ49Le9ob3",
        "livemode": false,
        "metadata": {},
        "reversals": {
            "object": "list",
            "data": [],
            "has_more": false,
            "total_count": 0,
            "url": "/v1/transfers/tr_1CkrRgJO26RVIZrdH1RYoqQj/reversals",
            "stripeResponse": null
        },
        "reversed": false,
        "sourceTransactionId": "py_1CkoVfJO26RVIZrd9esDbTrp",
        "source_type": "bank_account",
        "transfer_group": "bee8d641-e25c-4177-8b94-0e01450098d9",
        "id": "tr_1CkrRgJO26RVIZrdH1RYoqQj",
        "stripeResponse": null
}
</pre>


* **Error Response:**

    Code: 400 Bad Request
	<pre>	
    {
    "error": true,
    "valid": true,
    "message": "An internal server error occurred.",
    "data": null
	}
	</pre>
   

	
