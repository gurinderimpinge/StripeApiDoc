**Charge Amount Contractor Account Api**
----
Description : This will Charge Amount from Contractor Account.

* **URL**

   v1/stripe/ChargeAmount

* **Method:** 
    Post
	
* **Data Params** <br />

<pre>
 {
	  "amount": (int required), 
	  "description": "(string required)",
	  "currency": "(string required)",
	  "stripeCustomerId": "(string required)"
	  "receiptEmail": "(string required)" 
}	 
</pre>   

* **Example:** <br/>

<pre>
 {
	  "amount": 150,
	  "description": "Test By Api Method2ff",
	  "currency": "usd",
	  "stripeCustomerId": "cus_DAQnciDFSOAFN0",
	  "receiptEmail": "test@gmail.com"
 }
 </pre>
* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Amount of usd 150 has been charged",
    "error": null,
    "data": {
        "object": "charge",
        "amount": 150,
        "amount_refunded": 0,        
        "balanceTransactionId": "txn_1CkqHNJO26RVIZrdtu7SNDBx",
        "captured": true,
        "created": 1530869465,
        "currency": "usd",
        "customerId": "cus_DBBH5pF83Tsxnw",
        "description": "Test By Api Method2ff", 
        "paid": false,
        "receipt_email": "test@gmail.com",
        "status": "pending",
        "transferId": null,
        "transfer_group": "715ef81b-a12a-45c0-8f6a-d207bf76b549",
        "id": "py_1CkqHNJO26RVIZrd5iHcg8rl",
        "stripeResponse": null
    }   
}
</pre>

* **Error Response:**

    Code: 400 Bad Request
    <pre>
    {
      "message": "No such customer: {stripeCustomerId}"
    }
    </pre>  
    
 **Contractor ApiDoc:** <br/>
 
[Contractor Stripe CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ContractorStripeCreateAccount.md)
[Verify Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContractorAccount.md)
[Charge PaymentFrom ContractorAccount Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ChargeAmountContractorAccount.md)
[PaymentStatus Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/PaymentStatusContractorAccount.md)
[Delete Contractor stripe Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/DeleteContractorAccount.md)

**Contractee ApiDoc:** <br/>
 [Contractee Stripe CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ContracteeStripeCreateAccount.md)
[Delete Contractee Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/DeleteContracteeAccount.md)
[Transfer PaymentTo Contractee Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/TransferPaymentToContractee.md)
[Verify ContracteeAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContracteeAccount.md)

