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
<br />

**Login**
----
* **URL**

  http://travinesia.com:3000/v1/user/authenticate

* **Method:**

 `POST`
  
*  **URL Params**

   **Input(Required):**
 
   `email=[String]` <br />
   `password=[String]` <br />

   **Optional:**
 
   `token=will expired in 24h`

* **Data Params**

 NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** User authenticated! + token
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "Ensure your Email and Password are correct" }`

  OR

  * **Code:**  400 UNAUTHORIZED <br />
    **Content:** `{ error : "No password provided" }`

* **Notes:**

  Token will be expired in 24h

<br />

**Activate Account**
----
* **URL**

  http://travinesia.com:3000/v1/user/activate/:token

* **Method:**

 `PUT`
  
*  **URL Params**

   **Input(Required):**
 
  NONE

   **Optional:**
 
   NONE

* **Data Params**

  `req.params.token=[user.temporary token]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Account activated!
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "Activation link has expired." }`

* **Notes:**

  URL untuk parameter token akan didapatkan user dari email setelah register, lalu pada frontend atur pada routenya agar redirect ke halaman homepage dan memberkan respon susccess

<br />

**Send to Travinesia if User Forget the Password**
----
* **URL**

  http://travinesia.com:3000/v1/user/forgot_password

* **Method:**

 `PUT`
  
*  **URL Params**

   **Input(Required):**
   `email=[String]`

   **Optional:**
 
   NONE

* **Data Params**

  NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ "Please check your e-mail for password reset link." }`
 
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "E-mail was not found." }`

* **Notes:**

 Route ini berfungsi untuk User memberitahu kepada travinesia bawah user lupa password dan akan dikirimkan email berupa link untuk reset password

 <br />

 **URL for reset the Password**
----
* **URL**

  http://travinesia.com:3000/v1/user/forgot_password/:token

* **Method:**

 `GET`
  
*  **URL Params**

   **Input(Required):**
   NONE

   **Optional:**
 
   NONE

* **Data Params**

  `resettoken=[req.params.token]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** User email
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "Password link has expired" }`

* **Notes:**

 Route ini berguna untuk redirect ke halaman ubah Password

 **Save Password for User Forgot Password**
----
* **URL**

  http://travinesia.com:3000/v1/user/save_password

* **Method:**

 `PUT`
  
*  **URL Params**

   **Input(Required):**
   `email=[String]`
   `password=[String]`

   **Optional:**
 
   NONE

* **Data Params**

  NONE

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** Password has been reset!
* **Error Response:**

  * **Code:** 400 UNAUTHORIZED <br />
    **Content:** `{ error : "Password link has expired" }`

* **Notes:**

 Jika berhasil user akan menerima email telah berhasil