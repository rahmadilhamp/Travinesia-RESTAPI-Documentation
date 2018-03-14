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
<br />

**Change User Password**
----
* **URL**

  http://travinesia.com:3000/v1/user/change_password

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `password = [String]` <br />
   `new_password = [String]` 

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Password has been changed!

* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "Please insert your new password!" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />

**Register Provider**
----
* **URL**

  http://travinesia.com:3000/v1/user/register_provider

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `id_user = req.id_user from token` <br />
   `travel_name = [String]` <br />
   `slogan = [String]` <br />
   `description = [String]` <br />
   `office_address = [String]` <br />
   `province = [String]` <br /> 
   `office_phone_number = [String]` <br />
   `domain = [String]` <br />
   `logo = [String]` <br />

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Password has been changed!

* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : Provider registered and role has been changed!" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />

**Review Trip**
----
* **URL**

  http://travinesia.com:3000/v1/user/review/:id_booking

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `id_booking = (booking._id) From Booking Model` <br />
   `id_trip = (booking.id_trip) From Booking Model` <br />
   `field = [String]` <br />
   `rate = [String]`

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

    `id_booking = req.params.id_booking`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Successfully added rate and review!

* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : Make sure you give rate and review to the trip" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db



