**Delete Contractor Account Api**
----
Description : This will Delete Contractor Account.

* **URL**

   v1/stripe/DeleteContractorAccount/{id}

* **Method:** 
    Post
	

* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Contractor account has been deleted.",
    "error": null,
    "data": null,
    "token": null
}
</pre>


* **Error Response:**

    Code: 400 Bad Request
	<pre>
	{
    "message": "No such account against id: {id}"
    }
   
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
	

