**Create Contractee Account Api**
----
Description : This will Create new Contractee Account.

* **URL**

   v1/stripe/Contractee/CreateAccount

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
    "message": "New Contractee account has been created.",
    "error": null,
    "data": {
        "object": "account",
        "businessLogoFileId": null,
        "business_name": "Test",
        "business_primary_color": null,
        "business_url": null,
        "charges_enabled": true,
        "country": "US",
        "currencies_supported": null,
        "debit_negative_balances": false,
        "decline_charge_on": {
            "avs_failure": false,
            "cvc_failure": false,
            "stripeResponse": null
        },
        "default_currency": "usd",
        "details_submitted": true,
        "display_name": null,
        "email": "test@gmail.com",
        "external_accounts": {
            "object": "list",
            "data": [
                {
                    "type": 1,
                    "deleted": null,
                    "card": null,
                    "bankAccount": {
                        "object": "bank_account",
                        "account": "acct_1CkqoIAUuKd6japZ",
                        "account_holder_name": "Test",
                        "account_holder_type": "individual",
                        "bank_name": "STRIPE TEST BANK",
                        "country": "US",
                        "currency": "usd",
                        "customer": null,
                        "default_for_currency": true,
                        "fingerprint": "OoF5AVC1UPg30L4d",
                        "last4": "6789",
                        "metadata": {},
                        "routing_number": "110000000",
                        "status": "new",
                        "id": "ba_1CkqoIAUuKd6japZOrxghkUF",
                        "stripeResponse": null
                    },
                    "id": "ba_1CkqoIAUuKd6japZOrxghkUF",
                    "stripeResponse": null
                }
            ],
            "has_more": false,
            "total_count": 1,
            "url": "/v1/accounts/acct_1CkqoIAUuKd6japZ/external_accounts",
            "stripeResponse": null
        },
        "legal_entity": {
            "additional_owners": [],
            "address": {
                "city": "New York",
                "country": "US",
                "line1": "New York",
                "line2": null,
                "postal_code": "11003",
                "state": "New York",
                "town": null,
                "stripeResponse": null
            },            
            "business_name": "Test",          
            "business_tax_id_provided": true,
            "business_vat_id_provided": false,
            "dob": {
                "day": 15,
                "month": 5,
                "year": 1986,
                "stripeResponse": null
            },
            "first_name": "Test",
            "first_name_kana": null,
            "first_name_kanji": null,
            "gender": null,
            "last_name": "Test",
            "last_name_kana": null,
            "last_name_kanji": null,
            "maiden_name": null,
            "personal_address": {
                "city": null,
                "country": "US",
                "line1": null,
                "line2": null,
                "postal_code": null,
                "state": null,
                "town": null,
                "stripeResponse": null
            },
            "personal_address_kana": null,
            "personal_address_kanji": null,
            "personal_id_number_provided": true,
            "phone_number": null,
            "ssn_last_4_provided": true,
            "tax_id_registrar": null,
            "type": "individual",
            "verification": {
                "details": null,
                "details_code": null,
                "documentId": null,
                "documentIdBack": null,
                "status": "pending",
                "stripeResponse": null
            },
            "stripeResponse": null
        },       
        "product_description": null,
        "statement_descriptor": "",
        "support_email": null,
        "support_phone": null,
        "support_url": null,
        "timezone": "Etc/UTC",
        "tos_acceptance": {
            "date": 1520377200,
            "ip": "10.91.0.143",
            "user_agent": null,
            "stripeResponse": null
        },
        "type": "custom",
        "payouts_enabled": true,
        "payout_schedule": {
            "delay_days": 2,
            "interval": "daily",
            "monthly_anchor": 0,
            "weekly_anchor": null,
            "stripeResponse": null
        },
        "payout_statement_descriptor": null,
        "verification": {
            "disabled_reason": null,
            "due_by": null,
            "fields_needed": [],
            "stripeResponse": null
        },
        "keys": {
            "publishable": "pk_test_if1bmVeMKnKKhE229B8umty0",
            "secret": "sk_test_KORLWWZ4Yj8o1wypgrAeaaAI",
            "stripeResponse": null
        },
        "id": "acct_1CkqoIAUuKd6japZ",
        "stripeResponse": null
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
 **Contractor ApiDoc:** <br/>
[Contractor Stripe CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ContractorStripeCreateAccount.md)<br/>
[Verify Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContractorAccount.md)<br/>
[Charge PaymentFrom ContractorAccount Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ChargeAmountContractorAccount.md)<br/>
[PaymentStatus Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/PaymentStatusContractorAccount.md)<br/>
[Delete Contractor stripe Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/DeleteContractorAccount.md)

**Contractee ApiDoc:** <br/>
 [Contractee Stripe CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ContracteeStripeCreateAccount.md)<br/>
[Delete Contractee Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/DeleteContracteeAccount.md)<br/>
[Transfer PaymentTo Contractee Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/TransferPaymentToContractee.md)<br/>
[Verify ContracteeAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContracteeAccount.md)




	

