**Verify Contractor Account Api**
----
Description : Verify Contractor Account.

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
  {
    "status": true,
    "message": "Account has been verified",
    "error": null,
    "data": "verified",
    "token": null
}
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

	

