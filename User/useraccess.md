**GET Profile**
----
* **URL**

  http://travinesia.com:3000/v1/user/profile

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**
 
   NONE

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Data successfully + data:user
 
* **Error Response:**

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : "Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  NONE
<br />

**Edit Profile**
----
* **URL**

  http://travinesia.com:3000/v1/user/profile

* **Method:**

 `PUT`
  
*  **URL Params**

   **Input(Required):**
 
   `name = [String]` <br />
   `birthday = [Date]` <br />
   `gender = [String]` <br />
   `email = [String]` <br />
   `telephone = [String]` <br />
   `identity_number = [String]` <br />
   `photo = [String]` 

   **Optional:**
 
   NONE

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Data : User
 
* **Error Response:**

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  NONE

