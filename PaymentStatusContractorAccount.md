**Payment Status Contractor Account Api**
----
Description : This will check all the Payment status of the connected Contractor Id  and will update the status accordingly.

* **URL**

   v1/stripe/PaymentStatus

* **Method:** 
    Get	

* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Payment status has been updated.",
    "error": null,
    "data": null,
    "token": null
}
</pre>

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Payment status already up to date.",
    "error": null,
    "data": null,
    "token": null
}
</pre>

  **Create Account  ApiDoc:** <br/>
[Contractor Stripe CreateAccount ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/edit/master/CreateAccount.md)<br/>

**Verify Account  ApiDoc:** <br/>
[Verify Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/VerifyContractorAccount.md)<br/>

 **Contractor ApiDoc:** <br/>
[Charge PaymentFrom ContractorAccount Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/ChargeAmountContractorAccount.md)<br/>

 **PaymentStatus ApiDoc:** <br/>
[PaymentStatus Contractor Account ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/PaymentStatusContractorAccount.md)<br/>

**Contractee ApiDoc:** <br/>
[Transfer PaymentTo Contractee Apidoc ](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/TransferPaymentToContractee.md)<br/>

**Cards ApiDoc:** <br/>
[CardToken  ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/CardPaymentToken.md)<br/>
[CardPaymentCharge  ApiDoc](https://github.com/gurinderimpinge/StripeApiDoc/blob/master/CardPaymentChargeAccount.md)
	

