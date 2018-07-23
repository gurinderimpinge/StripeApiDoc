**Verify Account Api**
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
  "stripeCustomerId": "(string required)"  
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
    "message": "Account has been verified.",
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
    "message": "Account already verified.",
    "error": null,
    "data": null,
    "token": null
}
</pre>

* **Error Response:**

    Code: 400 Bad Request
 <pre>
  {
     "message": "There is no account against this contractor Id."
  }
  </pre>
  <br/>
     Code: 400 Bad Request
 <pre>
  {
     "message": "The amounts provided do not match the amounts that were sent to the bank account."
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
