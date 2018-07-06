**Verify Contractee Account Api**
----
Description : This will Verify Contractee Account.

* **URL**

   v1/stripe/VerifyContracteeAccount/{stripeConectedId}

* **Method:** 
    Get

* **Success Response:**

	Code: 200 
	
* **Content:**<br />
<pre>
{
    "status": true,
    "message": null,
    "error": null,
    "data": "verified",
    "token": null
}
</pre>

Code: 200 
	
* **Content:**<br />
<pre>
{
{
    "status": true,
    "message": "Account is already verified",
    "error": null,
    "data": null,
    "token": null
}
</pre>


