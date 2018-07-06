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
    "message": "Stripe account has been deleted",
    "error": null,
    "data": null,
    "token": null
}
</pre>

* **Error Response:**

    Code: 400 Bad Request
	<pre>
	{
    "message": "Account is not found"
}







