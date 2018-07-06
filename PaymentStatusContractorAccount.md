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
    "message": "Payment status has been updated",
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
    "message": "Payment status already up to date",
    "error": null,
    "data": null,
    "token": null
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

	

