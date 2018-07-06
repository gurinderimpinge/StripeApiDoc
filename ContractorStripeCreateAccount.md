**Stripe Create Contractor Account Api**
----
Description : Stripe Create Contractor Account.

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
    "message": "New Stripe account has been Created",
    "error": null,
    "data": {
        "object": "customer",       
        "created": 1530864206,
        "defaultSourceId": "ba_1CkouXJO26RVIZrdI9v0Myie",
        "delinquent": false,       
        "email": "gurinder.impinge@gmail.com",
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
    "message": "Account number is already exists"
    }

	</pre>
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


