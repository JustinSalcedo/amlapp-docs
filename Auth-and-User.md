---
title: Auth & User v1.0
language_tabs:
  - shell: Shell
  - javascript: JavaScript
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="auth-and-user">Auth & User v1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Before using AMLApp, you must authenticate the user and use his JSON Web Token to authorize every request. After authentication,  the user may get or edit his credentials and custom parameters.

Base URLs:

* <a href="https://amlapp.herokuapp.com/api">https://amlapp.herokuapp.com/api</a>

Email: <a href="mailto:web@justinsalcedo.com">web@justinsalcedo.com</a> Web: <a href="https://justinsalcedo.com">justinsalcedo.com</a> 
License: <a href="https://github.com/JustinSalcedo/amlapp/blob/master/LICENSE">MIT License</a>

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="auth-and-user-default">Endpoints</h1>

## post-auth-signup

<a id="opIdpost-auth-signup"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://amlapp.herokuapp.com/api/auth/signup \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'

```

```javascript
const inputBody = '{
  "name": "string",
  "email": "user@example.com",
  "password": "pa$$word"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'
};

fetch('https://amlapp.herokuapp.com/api/auth/signup',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

`POST /auth/signup`

*Create New User*

Register a new user.

> Body parameter

```json
{
  "name": "string",
  "email": "user@example.com",
  "password": "pa$$word"
}
```

<h3 id="post-auth-signup-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Content-Type|header|string|true|application/json|
|Accept|header|string|true|*/*|
|body|body|[New-User](#schemanew-user)|false|none|

> Example responses

> 201 Response

```json
{
  "user": {
    "role": "string",
    "custom_parameters": {
      "profit_margin": 0,
      "is_profit_percentage": true,
      "default_quantity": 0,
      "buying_mode": "string",
      "item_condition": "string",
      "listing_type_id": "string",
      "sale_terms": [
        {
          "id": "string",
          "value_name": "string"
        }
      ],
      "local_currency_code": "string",
      "sync_concurrency_in_hours": 0
    },
    "items": [
      {}
    ],
    "_id": "string",
    "name": "string",
    "email": "string",
    "createdAt": "string",
    "updatedAt": "string",
    "__v": 0
  },
  "token": "string"
}
```

<h3 id="post-auth-signup-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|User data and JWT token|Inline|

<h3 id="post-auth-signup-responseschema">Response Schema</h3>

Status Code **201**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» user|[User-Data](#schemauser-data)|true|none|none|
|»» role|string|false|none|none|
|»» custom_parameters|object|false|none|none|
|»»» profit_margin|integer|false|none|none|
|»»» is_profit_percentage|boolean|false|none|none|
|»»» default_quantity|integer|false|none|none|
|»»» buying_mode|string|false|none|none|
|»»» item_condition|string|false|none|none|
|»»» listing_type_id|string|false|none|none|
|»»» sale_terms|[object]|false|none|none|
|»»»» id|string|false|none|none|
|»»»» value_name|string|false|none|none|
|»»» local_currency_code|string|false|none|none|
|»»» sync_concurrency_in_hours|integer|false|none|none|
|»» items|[object]|false|none|none|
|»» _id|string|false|none|none|
|»» name|string|false|none|none|
|»» email|string|false|none|none|
|»» createdAt|string|false|none|none|
|»» updatedAt|string|false|none|none|
|»» __v|integer|false|none|none|
|» token|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## post-auth-signin

<a id="opIdpost-auth-signin"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://amlapp.herokuapp.com/api/auth/signin \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*'

```

```javascript
const inputBody = '{
  "email": "user@example.com",
  "password": "pa$$word"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*'
};

fetch('https://amlapp.herokuapp.com/api/auth/signin',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

`POST /auth/signin`

*Log In User*

Log in a returning user.

> Body parameter

```json
{
  "email": "user@example.com",
  "password": "pa$$word"
}
```

<h3 id="post-auth-signin-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Content-Type|header|string|true|application/json|
|Accept|header|string|true|*/*|
|body|body|[User-Credentials](#schemauser-credentials)|false|Email and password|

> Example responses

> 200 Response

```json
{
  "user": {
    "role": "string",
    "custom_parameters": {
      "profit_margin": 0,
      "is_profit_percentage": true,
      "default_quantity": 0,
      "buying_mode": "string",
      "item_condition": "string",
      "listing_type_id": "string",
      "sale_terms": [
        {
          "id": "string",
          "value_name": "string"
        }
      ],
      "local_currency_code": "string",
      "sync_concurrency_in_hours": 0
    },
    "items": [
      {}
    ],
    "_id": "string",
    "name": "string",
    "email": "string",
    "createdAt": "string",
    "updatedAt": "string",
    "__v": 0
  },
  "token": "string"
}
```

<h3 id="post-auth-signin-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User data and JWT token|Inline|

<h3 id="post-auth-signin-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» user|[User-Data](#schemauser-data)|true|none|none|
|»» role|string|false|none|none|
|»» custom_parameters|object|false|none|none|
|»»» profit_margin|integer|false|none|none|
|»»» is_profit_percentage|boolean|false|none|none|
|»»» default_quantity|integer|false|none|none|
|»»» buying_mode|string|false|none|none|
|»»» item_condition|string|false|none|none|
|»»» listing_type_id|string|false|none|none|
|»»» sale_terms|[object]|false|none|none|
|»»»» id|string|false|none|none|
|»»»» value_name|string|false|none|none|
|»»» local_currency_code|string|false|none|none|
|»»» sync_concurrency_in_hours|integer|false|none|none|
|»» items|[object]|false|none|none|
|»» _id|string|false|none|none|
|»» name|string|false|none|none|
|»» email|string|false|none|none|
|»» createdAt|string|false|none|none|
|»» updatedAt|string|false|none|none|
|»» __v|integer|false|none|none|
|» token|string|true|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## post-auth-logout

<a id="opIdpost-auth-logout"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://amlapp.herokuapp.com/api/auth/logout \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: Bearer {access-token}'

```

```javascript

const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'Bearer {access-token}'
};

fetch('https://amlapp.herokuapp.com/api/auth/logout',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

`POST /auth/logout`

*Log Out User*

Log out the current user.

<h3 id="post-auth-logout-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Content-Type|header|string|true|application/json|
|Accept|header|string|true|*/*|

<h3 id="post-auth-logout-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
UserJWT
</aside>

## post-user-profile-change-password

<a id="opIdpost-user-profile-change-password"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://amlapp.herokuapp.com/api/user/profile/change-password \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: Bearer {access-token}'

```

```javascript
const inputBody = '{}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'Bearer {access-token}'
};

fetch('https://amlapp.herokuapp.com/api/user/profile/change-password',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

`POST /user/profile/change-password`

*Change Password*

Change password through validation.

> Body parameter

```json
{}
```

<h3 id="post-user-profile-change-password-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Content-Type|header|string|true|application/json|
|Accept|header|string|true|*/*|
|body|body|object|false|none|

> Example responses

> 200 Response

```json
{
  "user": {
    "role": "string",
    "custom_parameters": {
      "profit_margin": 0,
      "is_profit_percentage": true,
      "default_quantity": 0,
      "buying_mode": "string",
      "item_condition": "string",
      "listing_type_id": "string",
      "sale_terms": [
        {
          "id": "string",
          "value_name": "string"
        }
      ],
      "local_currency_code": "string",
      "sync_concurrency_in_hours": 0
    },
    "items": [
      {}
    ],
    "_id": "string",
    "name": "string",
    "email": "string",
    "createdAt": "string",
    "updatedAt": "string",
    "__v": 0
  },
  "token": "string"
}
```

<h3 id="post-user-profile-change-password-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User data and JWT token|Inline|

<h3 id="post-user-profile-change-password-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» user|[User-Data](#schemauser-data)|true|none|none|
|»» role|string|false|none|none|
|»» custom_parameters|object|false|none|none|
|»»» profit_margin|integer|false|none|none|
|»»» is_profit_percentage|boolean|false|none|none|
|»»» default_quantity|integer|false|none|none|
|»»» buying_mode|string|false|none|none|
|»»» item_condition|string|false|none|none|
|»»» listing_type_id|string|false|none|none|
|»»» sale_terms|[object]|false|none|none|
|»»»» id|string|false|none|none|
|»»»» value_name|string|false|none|none|
|»»» local_currency_code|string|false|none|none|
|»»» sync_concurrency_in_hours|integer|false|none|none|
|»» items|[object]|false|none|none|
|»» _id|string|false|none|none|
|»» name|string|false|none|none|
|»» email|string|false|none|none|
|»» createdAt|string|false|none|none|
|»» updatedAt|string|false|none|none|
|»» __v|integer|false|none|none|
|» token|string|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
UserJWT
</aside>

## get-user-profile-data

<a id="opIdget-user-profile-data"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://amlapp.herokuapp.com/api/user/profile/data \
  -H 'Accept: */*' \
  -H 'Authorization: Bearer {access-token}'

```

```javascript

const headers = {
  'Accept':'*/*',
  'Authorization':'Bearer {access-token}'
};

fetch('https://amlapp.herokuapp.com/api/user/profile/data',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

`GET /user/profile/data`

*Get User Data*

Get user data, items, and custom settings.

<h3 id="get-user-profile-data-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Accept|header|string|true|*/*|

> Example responses

> 200 Response

```json
{
  "user": {
    "role": "string",
    "custom_parameters": {
      "profit_margin": 0,
      "is_profit_percentage": true,
      "default_quantity": 0,
      "buying_mode": "string",
      "item_condition": "string",
      "listing_type_id": "string",
      "sale_terms": [
        {
          "id": "string",
          "value_name": "string"
        }
      ],
      "local_currency_code": "string",
      "sync_concurrency_in_hours": 0
    },
    "items": [
      {}
    ],
    "_id": "string",
    "name": "string",
    "email": "string",
    "createdAt": "string",
    "updatedAt": "string",
    "__v": 0
  }
}
```

<h3 id="get-user-profile-data-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Example response|Inline|

<h3 id="get-user-profile-data-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» user|[User-Data](#schemauser-data)|false|none|none|
|»» role|string|false|none|none|
|»» custom_parameters|object|false|none|none|
|»»» profit_margin|integer|false|none|none|
|»»» is_profit_percentage|boolean|false|none|none|
|»»» default_quantity|integer|false|none|none|
|»»» buying_mode|string|false|none|none|
|»»» item_condition|string|false|none|none|
|»»» listing_type_id|string|false|none|none|
|»»» sale_terms|[object]|false|none|none|
|»»»» id|string|false|none|none|
|»»»» value_name|string|false|none|none|
|»»» local_currency_code|string|false|none|none|
|»»» sync_concurrency_in_hours|integer|false|none|none|
|»» items|[object]|false|none|none|
|»» _id|string|false|none|none|
|»» name|string|false|none|none|
|»» email|string|false|none|none|
|»» createdAt|string|false|none|none|
|»» updatedAt|string|false|none|none|
|»» __v|integer|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
UserJWT
</aside>

## patch-user-profile-data

<a id="opIdpatch-user-profile-data"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH https://amlapp.herokuapp.com/api/user/profile/data \
  -H 'Accept: */*' \
  -H 'Authorization: Bearer {access-token}'

```

```javascript

const headers = {
  'Accept':'*/*',
  'Authorization':'Bearer {access-token}'
};

fetch('https://amlapp.herokuapp.com/api/user/profile/data',
{
  method: 'PATCH',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

`PATCH /user/profile/data`

*Update Username and Email*

Update basic user credentials.

<h3 id="patch-user-profile-data-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Accept|header|string|true|*/*|

> Example responses

> 200 Response

```json
{
  "user": {
    "role": "string",
    "custom_parameters": {
      "profit_margin": 0,
      "is_profit_percentage": true,
      "default_quantity": 0,
      "buying_mode": "string",
      "item_condition": "string",
      "listing_type_id": "string",
      "sale_terms": [
        {
          "id": "string",
          "value_name": "string"
        }
      ],
      "local_currency_code": "string",
      "sync_concurrency_in_hours": 0
    },
    "items": [
      {}
    ],
    "_id": "string",
    "name": "string",
    "email": "string",
    "createdAt": "string",
    "updatedAt": "string",
    "__v": 0
  }
}
```

<h3 id="patch-user-profile-data-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Example response|Inline|

<h3 id="patch-user-profile-data-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» user|[User-Data](#schemauser-data)|false|none|none|
|»» role|string|false|none|none|
|»» custom_parameters|object|false|none|none|
|»»» profit_margin|integer|false|none|none|
|»»» is_profit_percentage|boolean|false|none|none|
|»»» default_quantity|integer|false|none|none|
|»»» buying_mode|string|false|none|none|
|»»» item_condition|string|false|none|none|
|»»» listing_type_id|string|false|none|none|
|»»» sale_terms|[object]|false|none|none|
|»»»» id|string|false|none|none|
|»»»» value_name|string|false|none|none|
|»»» local_currency_code|string|false|none|none|
|»»» sync_concurrency_in_hours|integer|false|none|none|
|»» items|[object]|false|none|none|
|»» _id|string|false|none|none|
|»» name|string|false|none|none|
|»» email|string|false|none|none|
|»» createdAt|string|false|none|none|
|»» updatedAt|string|false|none|none|
|»» __v|integer|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
UserJWT
</aside>

## get-user-profile-configuration-status

<a id="opIdget-user-profile-configuration-status"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://amlapp.herokuapp.com/api/user/profile/configuration-status \
  -H 'Accept: */*' \
  -H 'Authorization: Bearer {access-token}'

```

```javascript

const headers = {
  'Accept':'*/*',
  'Authorization':'Bearer {access-token}'
};

fetch('https://amlapp.herokuapp.com/api/user/profile/configuration-status',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

`GET /user/profile/configuration-status`

*Get User Configuration Status*

Check Amazon API and Mercado Libre account configuration status.

<h3 id="get-user-profile-configuration-status-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Accept|header|string|true|*/*|

> Example responses

> 200 Response

```json
{
  "configuration_status": {
    "configuration_complete": true,
    "mercado_libre_authorization": true,
    "rapidapi_key_added": true
  }
}
```

<h3 id="get-user-profile-configuration-status-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="get-user-profile-configuration-status-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» configuration_status|object|false|none|none|
|»» configuration_complete|boolean|false|none|none|
|»» mercado_libre_authorization|boolean|false|none|none|
|»» rapidapi_key_added|boolean|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
UserJWT
</aside>

# Schemas

<h2 id="tocS_New-User">New-User</h2>
<!-- backwards compatibility -->
<a id="schemanew-user"></a>
<a id="schema_New-User"></a>
<a id="tocSnew-user"></a>
<a id="tocsnew-user"></a>

```json
{
  "name": "string",
  "email": "user@example.com",
  "password": "pa$$word"
}

```

New-User

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|email|string(email)|true|none|none|
|password|string(password)|true|none|none|

<h2 id="tocS_User-Credentials">User-Credentials</h2>
<!-- backwards compatibility -->
<a id="schemauser-credentials"></a>
<a id="schema_User-Credentials"></a>
<a id="tocSuser-credentials"></a>
<a id="tocsuser-credentials"></a>

```json
{
  "email": "user@example.com",
  "password": "pa$$word"
}

```

User-Credentials

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string(email)|true|none|none|
|password|string(password)|true|none|none|

<h2 id="tocS_User-Data">User-Data</h2>
<!-- backwards compatibility -->
<a id="schemauser-data"></a>
<a id="schema_User-Data"></a>
<a id="tocSuser-data"></a>
<a id="tocsuser-data"></a>

```json
{
  "role": "string",
  "custom_parameters": {
    "profit_margin": 0,
    "is_profit_percentage": true,
    "default_quantity": 0,
    "buying_mode": "string",
    "item_condition": "string",
    "listing_type_id": "string",
    "sale_terms": [
      {
        "id": "string",
        "value_name": "string"
      }
    ],
    "local_currency_code": "string",
    "sync_concurrency_in_hours": 0
  },
  "items": [
    {}
  ],
  "_id": "string",
  "name": "string",
  "email": "string",
  "createdAt": "string",
  "updatedAt": "string",
  "__v": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|role|string|false|none|none|
|custom_parameters|object|false|none|none|
|» profit_margin|integer|false|none|none|
|» is_profit_percentage|boolean|false|none|none|
|» default_quantity|integer|false|none|none|
|» buying_mode|string|false|none|none|
|» item_condition|string|false|none|none|
|» listing_type_id|string|false|none|none|
|» sale_terms|[object]|false|none|none|
|»» id|string|false|none|none|
|»» value_name|string|false|none|none|
|» local_currency_code|string|false|none|none|
|» sync_concurrency_in_hours|integer|false|none|none|
|items|[object]|false|none|none|
|_id|string|false|none|none|
|name|string|false|none|none|
|email|string|false|none|none|
|createdAt|string|false|none|none|
|updatedAt|string|false|none|none|
|__v|integer|false|none|none|

