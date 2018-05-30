**Get Province Trip**
----
* **URL**

  http://travinesia.com:3000/get/province

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

   NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all province + data:AllProvince
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`
<br />

**Get Trip by Id Province**
----
* **URL**

  http://travinesia.com:3000/get/province/:id_province

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

   `id_province = req.params.id_province` //Id province, ex: 1, 2, 3 

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all Trip + data:province
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`
<br />

**Get Type Trip**
----
* **URL**

  http://travinesia.com:3000/get/type

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

   NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all type + data:AllType
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`
<br />

**Get Trip by Type**
----
* **URL**

  http://travinesia.com:3000/get/type/:id_type_trip

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

   `id_type_trip = req.params.id_type_trip` //id from Type ex: 1, 2, 3

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all trip + data:trip
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`
<br />

**Get Category Trip**
----
* **URL**

  http://travinesia.com:3000/get/category

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

   NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all category + data:AllCategory
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`
<br />

**Get Trip by Category**
----
* **URL**

  http://travinesia.com:3000/get/category/:category

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

   `category = req.params.category` //id from category ex : 1, 2, 3

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all trip + data:category
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`
<br />

**Get Facility Trip**
----
* **URL**

  http://travinesia.com:3000/get/facility

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

   NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all facility + data:AllFacility
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`
<br />


**Get Comment Trip Discussion**
----
* **URL**

  http://travinesia.com:3000/get/comment/:id

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

    `id = req.params.id` //Id Trip from mongodb 

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all comment + data:comment
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Get Trip Discussion**
----
* **URL**

  http://travinesia.com:3000/v1/get/discussion/:id

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

    `id = req.params.id` //Id Trip from mongodb 

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get all discussion + data:discussion
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Get Detail Trip**
----
* **URL**

  http://travinesia.com:3000/v1/get/detail_trip/:id_trip

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   NONE

* **Data Params**

    `id_trip = req.params.id_trip` //Id Trip from mongodb

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** succes get detail trip + data:detail
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

