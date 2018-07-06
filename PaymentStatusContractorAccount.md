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



	

