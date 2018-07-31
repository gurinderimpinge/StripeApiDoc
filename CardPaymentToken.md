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
  "profileId": "(string required)",
  "email": "(string required)",
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
</pre>
* **Success Response:**<br />
Code: 200 	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": null,
    "error": null,
    "data": {
        "object": "customer",
        "account_balance": 0,
        "bank_accounts": null,
        "business_vat_id": null,
        "created": 1532694406,
        "currency": null,
        "defaultCustomerBankAccountId": null,
        "defaultSourceId": "card_1CsV1sJO26RVIZrdj22ulTsI",
        "default_source_type": null,
        "deleted": null,
        "delinquent": false,
        "description": null,
        "discount": null,
        "email": "freelancer1@gmail.com",
        "invoice_prefix": "65E2941",
        "livemode": false,
        "metadata": {},
        "shipping": null,
        "sources": {
            "object": "list",
            "data": [
                {
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
                        "customerId": "cus_DJ7GpXtGlL3blq",
                        "cvc_check": "pass",
                        "default_for_currency": false,
                        "dynamic_last4": null,
                        "exp_month": 12,
                        "exp_year": 2022,
                        "fingerprint": "iNKOTdO5hDHKRzme",
                        "funding": "credit",
                        "last4": "4242",
                        "metadata": {},
                        "name": "Test freelancer2",
                        "recipientId": null,
                        "three_d_secure": null,
                        "tokenization_method": null,
                        "description": null,
                        "iin": null,
                        "issuer": null,
                        "id": "card_1CsV1sJO26RVIZrdj22ulTsI",
                        "stripeResponse": null
                    },
                    "deleted": null,
                    "sourceObject": null,
                    "id": "card_1CsV1sJO26RVIZrdj22ulTsI",
                    "stripeResponse": null
                }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/customers/cus_DJ7GpXtGlL3blq/sources",
            "stripeResponse": null
        },
        "subscriptions": {
            "object": "list",
            "data": [],
            "has_more": false,
            "total_count": 0,
            "url": "/v1/customers/cus_DJ7GpXtGlL3blq/subscriptions",
            "stripeResponse": null
        },
        "id": "cus_DJ7GpXtGlL3blq",
        "stripeResponse":null
        }
    },
    "token": null
}
</pre>
* **Error Response:** <br/>
Code: 400 Bad Request
<pre>	
{
   "message": "Your card number is incorrect."
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

