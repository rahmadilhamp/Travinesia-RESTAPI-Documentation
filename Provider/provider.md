**GET Profile Provider**
----
* **URL**

  http://travinesia.com:3000/v1/provider/profile

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**
 
   NONE

   **Optional:**
 
   `id_user = req.id_user` For get the Provider <br />
   `user_id = req.user_id` For get the User

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Get Profile Provider Success
 
* **Error Response:**

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : "Provider Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  id_user = req.id_user diambil dari token
<br />

**Edit Profile Provider**
----
* **URL**

  http://travinesia.com:3000/v1/provider/profile

* **Method:**

 `PUT`
  
*  **URL Params**

   **Input(Required):**
 
   `travel_name = [String]` <br />
   `slogan = [String]` <br />
   `description = [String]` <br />
   `office_address = [String]` <br />
   `province = [String]` <br /> 
   `office_phone_number = [String]` <br />
   `domain = [String]` <br />
   `logo = [String]` <br />

   **Optional:**
 
   `id_user = req.id_user` For get the Provider <br />
   `user_id = req.user_id` For get the User


* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Your Provider Profile Has Been Updated!

* **Error Response:**

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : "Provider Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  id_user = req.id_user diambil dari token
<br />

**Add Trip Provider**
----
* **URL**

  http://travinesia.com:3000/v1/provider/add_trip

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `trip_name = [String]` <br />
   `id_type_trip = [String]` <br />
   `days = [String]` <br />
   `night = [String]` <br />
   `date_trip = [String]` <br /> 
   `publish_price = [Number]` <br />
   `fixed_price = [Number]` <br />
   `service_fee = [Number]` <br />
   `quota_trip = [Number]` <br />
   `description = [String]` <br />
   `notes_traveler = [String]` <br />
   `id_category = [String]` <br />
   `id_facility = [String]` <br />
   `id_status_trip = [1,1,1,1,1]` <br />
   `publish_price_group = [String]` <br />
   `service_fee_group = [String]` <br />
   `fixed_price_grorup = [String]` <br />
   `photo_trip = [String]`

   **Optional:**
 
   `id_user = req.id_user` For get the Provider <br />
   `user_id = req.user_id` For get the User


* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Trip registered!
    
* **Error Response:**

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : "Provider Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  id_user = req.id_user diambil dari token <br />
  user_id = req.user_id
<br />

**Add Trip Provider**
----
* **URL**

  http://travinesia.com:3000/v1/provider/edit_trip/:id

* **Method:**

 `PUT`
  
*  **URL Params**

   **Input(Required):**
 
   `trip_name = [String]` <br />
   `id_type_trip = [String]` <br />
   `days = [String]` <br />
   `night = [String]` <br />
   `date_trip = [String]` <br /> 
   `publish_price = [Number]` <br />
   `fixed_price = [Number]` <br />
   `service_fee = [Number]` <br />
   `quota_trip = [Number]` <br />
   `description = [String]` <br />
   `notes_traveler = [String]` <br />
   `id_category = [String]` <br />
   `id_facility = [String]` <br />
   `id_status_trip = [1,1,1,1,1]` <br />
   `publish_price_group = [String]` <br />
   `service_fee_group = [String]` <br />
   `fixed_price_grorup = [String]` <br />
   `photo_trip = [String]`

   **Optional:**
 
   `id_user = req.id_user` For get the Provider <br />
   `user_id = req.user_id` For get the User


* **Data Params**

 `id = req.params.id` //trip._id

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Your Trip Has Been Updated!
    
* **Error Response:**

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : "Provider Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

  OR

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : "Trip Not Found" }`

* **Notes:**

  id_user = req.id_user diambil dari token <br />
  user_id = req.user_id <br />
  trip._id = _id trip from mongodb
<br />

**Get Trip Provider**
----
* **URL**

  http://travinesia.com:3000/v1/provider/all_trip 

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**
 
   NONE

   **Optional:**
 
   `id_user = req.id_user` For get the Provider <br />
   `user_id = req.user_id` For get the User

* **Data Params**

   NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Trip Removed!
 
* **Error Response:**

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : Error in deleting trip }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  id_user = decoded from token 
  user_id = decoded from token
<br />

**GET Profile Provider**
----
* **URL**

  http://travinesia.com:3000/v1/provider/profile

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**
 
   NONE

   **Optional:**
 
   `id_user = req.id_user` For get the Provider <br />
   `user_id = req.user_id` For get the User

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Get Trip Provider Success

* **Error Response:**

  * **Code:** 404 UNAUTHORIZED <br />
    **Content:** `{ error : "Provider Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  id_user = req.id_user decoded from token
  user_id = req.user_id decoded from token
<br />




