**POST Discussion**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/post/:id_trip

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `id_trip=[Req.params.id_trip]` <br />
   `id_user=[req.id_user]` <br />
   `content=[String]` <br /> 

   **Optional:**
 
   `req.id_user=Decoded from token`
   `req.user_id=Decoded from token`

* **Data Params**

    `id_trip = req.params.id_trip` //Id Trip from mongodb 

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Success added the discussion + data=user + discussion=discussion.content + created=discussion.created_at
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : Trip Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Edit Discussion**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/edit/:id

* **Method:**

 `PUT`
  
*  **URL Params**

   **Input(Required):**

   `content=[String]`

   **Optional:**
 
   `req.id_user=Decoded from token`
   `req.user_id=Decoded from token`

* **Data Params**

    `id = req.params.id` //Id Discussion from mongodb 

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Discussion Edited + data=user + discussion=discussion.content + updatedd=discussion.updated
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : Discussion Not Found" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Delete Discussion**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/delete/:id

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**
 
   `req.id_user=Decoded from token`
   `req.user_id=Decoded from token`

* **Data Params**

    `id = req.params.id` //Id Discussion from mongodb 

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Discussion deleted!
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : Error in deleting discussion" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Get Trip Discussion**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/trip_discussion/:id

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

**Post Comment**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/post_comment

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**

   `id_discussion=[String]` //Id diskusi yang akan dikomen <br />
   `id_trip=discussion.trip` //From attribute Discussion <br />
   `id_user=req.id_user` //Decoded from token <br />
   `comment=[String]` <br />
   `discussion.id_trip` //To find the Trip

   **Optional:**
 
   NONE

* **Data Params**

   NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Comment added successfully + data:provider + comment:comment.comment + created:comment.created_at <br />
    If Provider post a comment <br />

  OR

  * **Code:** 200 <br />
    **Content:** Comment added successfully + data:user + comment:comment.comment + created:comment.created_at <br />
    If User post a comment 
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Edit Comment**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/edit_comment/:id

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**

   `id_discussion=[String]` //Id diskusi yang akan dikomen <br />
   `id=req.params.id` //Id comment yang akan diubah <br />
   `id_trip=discussion.trip` //From attribute Discussion <br />
   `id_user=req.id_user` //Decoded from token <br />
   `comment=[String]` <br />
   `discussion.id_trip` //To find the Trip

   **Optional:**
 
   NONE

* **Data Params**

   NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Comment successfully changed + data:provider + comment:comment.comment + created:comment.created_at <br />
    If Provider post a comment <br />

  OR

  * **Code:** 200 <br />
    **Content:** Comment successfully changed + data:user + comment:comment.comment + created:comment.created_at <br />
    If User post a comment 
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Delete Comment**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/delete_comment/:id_discussion/:id

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**

   NONE

   **Optional:**

   `req.user_id=Decoded from token`

* **Data Params**

    `id = req.params.id` //Id Comment from mongodb 
    `id_discussion = req.params.id_discussion` //Id Discussion thath will be comment

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Comment Removed!
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : Error in deleting comment" }`

  OR

  * **Code:** 403 PROHIBITED <br />
    **Content:** `{ error : "Forbidden access for this user" }`
<br />

**Get Comment Trip Discussion**
----
* **URL**

  http://travinesia.com:3000/v1/discussion/trip_comment/:id

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