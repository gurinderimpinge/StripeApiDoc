**Verify Contractor Account Api**
----
Description : This will Verify Contractor Account.

* **URL**

   v1/stripe/VerifyAccount

* **Method:** 
    Post
	
* **Data Params** <br />

<pre>
{
  "amountOne": (int required), 
  "amountTwo": "(int required)",
  "stripeCustomerId": "(string required)",
  "bankId": "(string required)" 
}	 
</pre>   

* **Example:** <br/>

<pre>

  {
  "amountOne": 32,
  "amountTwo": 45,
  "stripeCustomerId": "cus_DB9xvlmdH53o2M",
  "bankId": "ba_1CknduJO26RVIZrdtBj57YDR"  
  }

</pre> 
* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{ 
    "status": true,
    "message": "Account has been verified",
    "error": null,
    "data": "verified",
    "token": null
}
</pre>

Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": "Account already verified",
    "error": null,
    "data": null,
    "token": null
}
</pre>

* **Error Response:**

    Code: 400 Bad Request
	<pre>
	{
     "message": "There is no account against this contractor Id"
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
