**Delete Contractor Account Api**
----
Description : Delete Contractor Account.

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
    "message": "Account has been verified",
    "error": null,
    "data": "verified",
    "token": null
}
</pre>


* **Error Response:**

    Code: 400 Bad Request
	<pre>
	{
    "message": "No such account against id: {id}"
    }
   

	

