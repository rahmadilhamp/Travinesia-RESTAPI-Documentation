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

**Add Booking User**
----
* **URL**

  http://travinesia.com:3000/v1/user/addbooking

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `user_id = req.user_id from token` <br />
   `id_trip = [String]` <br />
   `id_paymentMethod = [String]` <br />
   `id_statusPayment = [String]` <br />
   `order_name = [String]` <br />
   `quantity = [Number]` <br /> 
   `name_traveller = [String]` <br />
   `identity_number = [Number]` <br />
   `startDate_trip = [Date]` <br />
   `endDate_trip = [Date]` <br />
   `uniq_code = [String]` <br />
   `expired = [String]` <br />

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** BOOKING berhasil!

* **Error Response:**

  * **Code:** 500 <br />
    **Content:** `{ error }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />

**Add Billing User**
----
* **URL**

  http://travinesia.com:3000/v1/user/billing

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `From Payment Gateway` <br />
   `id_booking = [String]`

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** billing berhasil!

* **Error Response:**

  * **Code:** 500 <br />
    **Content:** `{ error }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />


**Add Promo User**
----
* **URL**

  http://travinesia.com:3000/v1/user/addPromo

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `title = [String]` <br />
   `description = [String]` <br />
   `kode_promo = [String]` <br />
   `expired = [String]` <br />
   `flag_promo = [String]` <br />
   `photo_promo = [String]` <br />
   `nominal = [Number]`

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Promo berhasil ditambahkan

* **Error Response:**

  * **Code:** 500 <br />
    **Content:** `{ error }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />

**Delete Promo User**
----
* **URL**

  http://travinesia.com:3000/v1/user/deletepromo/:id_promo

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

  `promo = req.params.promo` dari id mongo atau id promo ex: 1, 2, 3

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Promo Removed

* **Error Response:**

  * **Code:** 404 <br />
    **Content:** `{ error : Error Deleting Promo }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />

**Get Booking User**
----
* **URL**

  http://travinesia.com:3000/v1/user/update_status/:id_booking

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Success get Booking, data:bookinguser

* **Error Response:**

  * **Code:** 404 <br />
    **Content:** `{ error : "" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />

**Isi Data Peserta**
----
* **URL**

  http://travinesia.com:3000/v1/user/isidatapeserta/:id_booking

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
   `identity_number = [String]` <br />
   `age_traveller = [String]` <br />
   `name_traveller = [String]`

   **Optional:**
 
   `req.user_id = from token`

* **Data Params**
  `id_booking = req.params.id_booking` id booking ex: 1, 2, 3
* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Isi data peserta sukses, data:booking

* **Error Response:**

  * **Code:** 404 <br />
    **Content:** `{ error : "" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user + token:req.token" }`

* **Notes:**

  req.user_id = from token untuk mencari user didalam db
<br />



