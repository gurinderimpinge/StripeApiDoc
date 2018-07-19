**Delete Contractee Account Api**
----
Description : This will delete Contractee Account.

* **URL**

   v1/stripe/DeleteContracteeAccount/{id}

* **Method:** 
    Get

* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Contractee account has been deleted.",
    "error": null,
    "data": null,
    "token": null
}
</pre>

* **Error Response:**

    Code: 400 Bad Request
<pre>
{
    "message": "Account not found."
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
[Verify ContracteeAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContracteeAccount.md)<br/>
**Cards ApiDoc:** <br/>
[CardToken  ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/CardPaymentToken.md)<br/>
[CardPaymentCharge  ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/CardPaymentChargeAccount.md)





