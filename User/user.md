**Register API**
----
* **URL**

  http://travinesia.com:3000/v1/user/users

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `name=[String]`
   `telephone=[String]`
   `email=[String]`
   `password=[String]`

   **Optional:**
 
   `temporarytoken=from JWT Token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Account registered! Please check your e-mail for activation link.
 
* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "Ensure your email and password were provided" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "That email as already taken" }`

* **Sample Call:**

  NONE

* **Notes:**

  NONE