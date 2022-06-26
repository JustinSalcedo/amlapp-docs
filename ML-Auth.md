---
title: ML-Auth v1.0
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

<h1 id="ml-auth">ML-Auth v1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

AMLApp generates the redirection URL for the user to sign in his Mercado Libre account and authorize the App to publish items in the user's behalf.

Base URLs:

* <a href="https://amlapp.herokuapp.com/api">https://amlapp.herokuapp.com/api</a>

Email: <a href="mailto:web@justinsalcedo.com">web@justinsalcedo.com</a> Web: <a href="https://justinsalcedo.com">justinsalcedo.com</a> 
License: <a href="https://github.com/JustinSalcedo/amlapp/blob/master/LICENSE">MIT License</a>

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="ml-auth-default">Endpoints</h1>

## get-ml-access

<a id="opIdget-ml-access"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://amlapp.herokuapp.com/api/ml/access?origin_url=https%3A%2F%2Fapp-client.com%2Fdashbord \
  -H 'Accept: */*' \
  -H 'Authorization: Bearer {access-token}'

```

```javascript

const headers = {
  'Accept':'*/*',
  'Authorization':'Bearer {access-token}'
};

fetch('https://amlapp.herokuapp.com/api/ml/access?origin_url=https%3A%2F%2Fapp-client.com%2Fdashbord',
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

`GET /ml/access`

*Get Auth URL*

Request an authorized URL and redirect the user to log into Mercado Libre.

<h3 id="get-ml-access-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Accept|header|string|true|*/*|
|origin_url|query|string(uri)|true|Redirect the user to this URL once authenticated|

> Example responses

> OK

```json
{
  "redirectUrl": "https://auth.mercadolibre.com.mx/authorization?response_type=code&client_id=0205730184629437&state=https://app-client.com/dashboard/b62b0016023dd8145356ebd3/295529&redirect_uri=https://amlapp.herokuapp.com/ml/auth"
}
```

<h3 id="get-ml-access-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="get-ml-access-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» redirectUrl|string(uri)|true|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
UserJWT
</aside>

## get-ml-auth

<a id="opIdget-ml-auth"></a>

> Code samples

```shell
# You can also use wget
curl -X GET https://amlapp.herokuapp.com/api/ml/auth?code=TG-062492b365cfae001328csdhc-1148675665&state=string \
  -H 'Accept: */*'

```

```javascript

const headers = {
  'Accept':'*/*'
};

fetch('https://amlapp.herokuapp.com/api/ml/auth?code=TG-062492b365cfae001328csdhc-1148675665&state=string',
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

`GET /ml/auth`

*Auth Redirection (by ML server)*

Once authenticated, Mercado Libre redirects the user agent to this endpoint to exchange the access code; this route is referenced for developmental purposes only.

<h3 id="get-ml-auth-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Accept|header|string|true|*/*|
|code|query|string|true|ML access code|
|state|query|string|true|Stablish flow security|

<h3 id="get-ml-auth-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|302|[Found](https://tools.ietf.org/html/rfc7231#section-6.4.3)|Found. Redirect to client URL once authenticated.|None|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

