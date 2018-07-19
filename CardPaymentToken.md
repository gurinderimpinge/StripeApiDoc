**Card Token Api**
----
Description : This will create Card Token to make Card Payment.

* **URL**

   v1/stripe/CardToken

* **Method:** 
    Post
	
* **Data Params** <br />
<pre>
{
  "CardNumber": "(string required)",
  "ExpirationYear": (int required), 
  "ExpirationMonth": (int required),  
  "Cvc": "(string required)",
  "Name": "(string required)",  
   "AddressCity": "(string )",
  "AddressCountry": "(string )",  
   "AddressLine1": "(string )",
  "AddressLine2": "(string )",  
   "AddressState": "(string )",
  "AddressZip": "(string )",  
   "Currency": "(string )"   
}
</pre>  

* **Example:** <br/>
<pre>

 {
  "CardNumber" : "4242424242424242",
  "ExpirationYear" : 22,
  "ExpirationMonth" : 12,
  "Cvc" :"123",
  "Name" : "Test Name"
 }
* **Success Response:**

	Code: 200 	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Card Token has been created",
    "error": null,
    "data": {
        "object": "token",
        "bank_account": null,
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
            "cvc_check": "unchecked",
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
            "id": "card_1CpYe7JO26RVIZrdGMGH8DOU",
            "stripeResponse": null
        },
        "client_ip": "202.164.36.12",
        "created": 1531993323,
        "livemode": false,
        "type": "card",
        "used": false,
        "description": null,
        "id": "tok_1CpYe7JO26RVIZrdCQf3Xfxn",
        "stripeResponse": { }
    },
    "token": null
}
</pre>

* **Error Response:**
Code: 400 Bad Request
<pre>	
{
   "message": "Your card number is incorrect."
}	
</pre>
