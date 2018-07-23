**Create  Account Api**
----
Description : This will Create new Account.

* **URL**

   v1/stripe/CreateAccount

* **Method:** 
    Post
	
 **Data Params** <br />

<pre>
{
  "email": "(string)",
  "type": "(string)",
  "tosAcceptanceDate": "(string required)",
  "tosAcceptanceIp": "(string required)",
  "externalBankAccount": {
  "accountHolderName":"(string required)",
  "accountHolderType": "(string required)",
  "accountNumber": "(string required)",
  "routingNumber": "(string required)",
  "country": "(string required)",
  "currency": "(string required)",
},
  "businessName": "(string)",
  "profileId": "(string required)",
  "country": "(string)",
  "legalEntity": {
     "type":"(string)",
  "firstName": "(string)",
  "lastName": "(string)",
  "birthDay": "(int required)",
  "birthMonth": "(int required)",
  "birthYear": "(int required)",
  "businessTaxId": "(string)",
  "businessName": "(string )",
  "addressCity":"(string )",
  "addressState":"(string )",
  "addressLine1": "(string )",
  "ssnLast4": "(string)",
  "personalIdNumber": "(string )",
  "addressPostalCode": "(string )",
    "country": "(string )",
},
  
 "Identitybase64format": "(string required)",
}
 
</pre>   

* **Example:** <br/>


<pre>
 {
  "email": "test@gmail.com",
  "type": "custom", * **The Stripe account type. Can be standard, express, or custom **
  "tosAcceptanceDate": "03-07-2018",
  "tosAcceptanceIp": "10.91.0.143",
  "externalBankAccount": {
  "accountHolderName": "Test",
  "accountHolderType": "individual",
  "accountNumber": "000123456789",
  "routingNumber": "110000000",
  "country": "us",
  "currency": "usd"
},
  "businessName": "Test",
  "profileId":"64646464",
  "country": "us",
  "legalEntity": {
     "type": "individual",
  "firstName": "Test",
  "lastName": "Test",
  "birthDay": 15,
  "birthMonth": 05,
  "birthYear": 1986,
  "businessTaxId": "BusinessTaxId",
  "businessName": "Test",
  "addressCity": "New York",
  "addressState": "New York",
  "addressLine1": "New York",
  "ssnLast4": "4199",
  "personalIdNumber": "472174199",
  "addressPostalCode": "11003",
    "country": "us",
},
  
 "Identitybase64format": "base64"
}
</pre>	

* **Success Response:**

	Code: 200 
	
* **Content:**<br />

<pre>
{
    "status": true,
    "message": "New account has been created.",
    "error": null,
    "data": {
        "object": "customer",
        "account_balance": 0,
        "bank_accounts": null,
        "business_vat_id": null,
        "created": 1532352168,
        "currency": null,
        "defaultCustomerBankAccountId": null,
        "defaultSourceId": "ba_1Cr3zvJO26RVIZrdTJHnozIJ",
        "default_source_type": null,
        "deleted": null,
        "delinquent": false,
        "description": null,
        "discount": null,
        "email": "TestGurinder@gmail.com",
        "invoice_prefix": "D627276",
        "livemode": false,
        "metadata": {},
        "shipping": null,
        "sources": {
            "object": "list",
            "data": [
                {
                    "type": 1,
                    "account": null,
                    "bankAccount": {
                        "object": "bank_account",
                        "account": null,
                        "account_holder_name": "Varinder",
                        "account_holder_type": "individual",
                        "bank_name": "STRIPE TEST BANK",
                        "country": "US",
                        "currency": "usd",
                        "customer": "cus_DHdGfoj3IYh7Dh",
                        "default_for_currency": false,
                        "fingerprint": "mzwBnKpN8XoKdWlD",
                        "last4": "4440",
                        "metadata": {},
                        "routing_number": "110000000",
                        "status": "new",
                        "id": "ba_1Cr3zvJO26RVIZrdTJHnozIJ",
                        "stripeResponse": null
                    },
                    "card": null,
                    "deleted": null,
                    "sourceObject": null,
                    "id": "ba_1Cr3zvJO26RVIZrdTJHnozIJ",
                    "stripeResponse": null
                }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/customers/cus_DHdGfoj3IYh7Dh/sources",
            "stripeResponse": null
        },
        "subscriptions": {
            "object": "list",
            "data": [],
            "has_more": false,
            "total_count": 0,
            "url": "/v1/customers/cus_DHdGfoj3IYh7Dh/subscriptions",
            "stripeResponse": null
        },
        "id": "cus_DHdGfoj3IYh7Dh",
        "stripeResponse":null
}
</pre>

* **Error Response:**

    Code: 400 Bad Request
<pre>
{
    "error": false,
    "valid": false,
    "message": "The request is invalid.",
    "data": {
        "model.Country": [
            "The Country field is required."
        ],
        "model.Identitybase64format": [
            "The Identitybase64format field is required."
        ],
        "model.LegalEntity.Type": [
            "The Type field is required."
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

	

