---
title: Amazon-Auth v1.0
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

<h1 id="amazon-auth">Amazon-Auth v1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

The Axesso's Amazon web scrapper gives us access to bulk product views in real-time. We can lookup for product details and more useful data. Documentation can be found at http://api-doc.axesso.de/#api-Amazon.

Base URLs:

* <a href="https://amlapp.herokuapp.com/api">https://amlapp.herokuapp.com/api</a>

Email: <a href="mailto:web@justinsalcedo.com">web@justinsalcedo.com</a> Web: <a href="https://justinsalcedo.com">justinsalcedo.com</a> 
License: <a href="https://github.com/JustinSalcedo/amlapp/blob/master/LICENSE">MIT License</a>

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="amazon-auth-default">Endpoints</h1>

## post-amazon-auth-add-api-key

<a id="opIdpost-amazon-auth-add-api-key"></a>

> Code samples

```shell
# You can also use wget
curl -X POST https://amlapp.herokuapp.com/api/amazon/auth/add-api-key \
  -H 'Content-Type: application/json' \
  -H 'Accept: */*' \
  -H 'Authorization: Bearer {access-token}'

```

```javascript
const inputBody = '{
  "rapidapi_key": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'*/*',
  'Authorization':'Bearer {access-token}'
};

fetch('https://amlapp.herokuapp.com/api/amazon/auth/add-api-key',
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

`POST /amazon/auth/add-api-key`

*Add API Key*

Add RapidAPI key to access Axesso's API.

> Body parameter

```json
{
  "rapidapi_key": "string"
}
```

<h3 id="post-amazon-auth-add-api-key-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Content-Type|header|string|true|application/json|
|Accept|header|string|true|*/*|
|body|body|object|false|none|
|» rapidapi_key|body|string|true|none|

> Example responses

> 200 Response

```json
{
  "message": "string"
}
```

<h3 id="post-amazon-auth-add-api-key-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="post-amazon-auth-add-api-key-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» message|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
UserJWT
</aside>
