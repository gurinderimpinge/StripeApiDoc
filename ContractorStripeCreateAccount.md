**Create Contractor Account Api**
----
Description : This will Create new Contractor Account.

* **URL**

   v1/stripe/Contractor/CreateAccount

* **Method:** 

    Post
* **Data Params** <br />

<pre>
{
   "email": (string required),
  "type": "custom",
  "country": "(string required)",
  "accountHolderName": "(string required)",
  "accountHolderType": "individual",
  "accountNumber": "(integer required)",
  "routingNumber": "(integer required)",
  "currency": "string  required",
  "token":"null" 
}	 
</pre>   

* **Example:** <br/>

<pre>
{
   "email": "123@gmail.com",
  "type": "custom",
  "country": "US",
  "accountHolderName": "Test",
  "accountHolderType": "individual",
  "accountNumber": "000123456789",
  "routingNumber": "110000000",
  "currency": "usd",
  "token":"null"
}
</pre> 
* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "New Contactor account has been Created.",
    "error": null,
    "data": {
        "object": "customer",       
        "created": 1530864206,
        "defaultSourceId": "ba_1CkouXJO26RVIZrdI9v0Myie",
        "delinquent": false,       
        "email": "test@gmail.com",
        "invoice_prefix": "E0BBC23",        
        "sources": {
            "object": "list",
            "data": [
                {
                    "type": 1,                   
                    "bankAccount": {
                        "object": "bank_account",
                        "account": null,
                        "account_holder_name": "Gurinder",
                        "account_holder_type": "individual",
                        "bank_name": "STRIPE TEST BANK",
                        "country": "US",
                        "currency": "usd",
                        "customer": "cus_DBBH5pF83Tsxnw",
                        "default_for_currency": false,
                        "fingerprint": "UN37sOWXjzRLKQxs",
                        "last4": "6789",
                        "metadata": {},
                        "routing_number": "110000000",
                        "status": "new",
                        "id": "ba_1CkouXJO26RVIZrdI9v0Myie",
                        "stripeResponse": null
                    },                  
                    "id": "ba_1CkouXJO26RVIZrdI9v0Myie",
                }
            ],
         },
       
        "id": "cus_DBBH5pF83Tsxnw",
        "stripeResponse": null
    },
    "token": null
}
</pre>
* **Error Response:**

    Code: 400 Bad Request
<pre>
{
    "message": "Account number already exists."
}
</pre><br />

     Code: 400 Bad Request
<pre>
{
    "error": false,
    "valid": false,
    "message": "The request is invalid.",
    "data": {
        "model.Email": [
            "The Email field is required.",
            "The Email field is not a valid e-mail address."
        ],
        "model.Type": [
            "The Type field is required."
        ],
        "model.Country": [
            "The Country field is required."
        ],
        "model.AccountHolderName": [
            "The AccountHolderName field is required."
        ],
        "model.AccountHolderType": [
            "The AccountHolderType field is required."
        ],
        "model.AccountNumber": [
            "The AccountNumber field is required."
        ],
        "model.RoutingNumber": [
            "The RoutingNumber field is required."
        ],
        "model.Currency": [
            "The Currency field is required."
        ],
        "model.Token": [
            "The Token field is required."
        ]
    }
}
</pre>


  Code: 400 Bad Request
<pre>
{    
    "message": "Account already exists."
}
</pre>

 **Contractor ApiDoc:** <br/>
[Contractor Stripe CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ContractorStripeCreateAccount.md)<br/>
[Verify Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContractorAccount.md)<br/>
[Charge PaymentFrom ContractorAccount ApiDoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ChargeAmountContractorAccount.md)<br/>
[PaymentStatus Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/PaymentStatusContractorAccount.md)<br/>
[Delete Contractor stripe Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/DeleteContractorAccount.md)

**Contractee ApiDoc:** <br/>
 [Contractee Stripe CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ContracteeStripeCreateAccount.md)<br/>
[Delete Contractee Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/DeleteContracteeAccount.md)<br/>
[Transfer PaymentTo Contractee ApiDoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/TransferPaymentToContractee.md)<br/>
[Verify ContracteeAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContracteeAccount.md)
