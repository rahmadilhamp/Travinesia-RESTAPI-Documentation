**Register API**
----
* **URL**

  http://travinesia.com:3000/v1/user/users

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `name=[String]` <br />
   `telephone=[String]` <br />
   `email=[String]` <br />
   `password=[String]` <br />

   **Optional:**
 
   `temporarytoken=from JWT Token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Account registered! Please check your e-mail for activation link.
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "Ensure your email and password were provided" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "That email as already taken" }`

* **Sample Call:**

  NONE

* **Notes:**

  NONE