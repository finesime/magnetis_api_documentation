--- 

title: magnetis 

language_tabs: 
  - shell: cURL
  - php: PHP
  - javascript: JavaScript

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true
--- 

# Introduction

**API - Magnetis**

**Endpoint URL:** https://www.magnetis-in.com/v1/

**Version:** v1

See more at [Magnetis API Support](https://www.magnetis.fr/console/support/api/)

Contact the [developer](mailto:support@magnetis.fr?subject=API-Magnetis) here.

# /ACCOUNTS
## ***GET*** 

>To Authorize and request account information, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "idacc": {
	    "company_name": "string",
	    "email": "string",
	    "plan": "string"
	  }
    },
    ...
]
```


### HTTP Request 
`***GET*** /accounts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |
| 400 | 400 response |
| 401 | 401 response |

# /ACCOUNTS/CHROME
## ***GET*** 

### HTTP Request 
`***GET*** /accounts/chrome` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/chrome` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/KPI
## ***GET*** 

>To Authorize and retrieve account kpi, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/kpi 
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/kpi",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/kpi",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "idacc": {
	    "call": number,
	    "time": number,
	    "lost": number
	  }
	}
]
```

### HTTP Request 
`***GET*** /accounts/kpi` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| DateTo | query |  | No | string |
| DateFrom | query |  | No | string |
| limit | query |  | No | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/kpi` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/CALLBYDAY
## ***GET*** 

>To Authorize and retrieve calls by day, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/callbyday
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/callbyday",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/callbyday",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "day": {
	    "jour": "string",
	    "numeros": {
	      "idnumber": {
	        "numnumero": number,
	        "supportnumero": "string",
	        "numero": "string",
	        "NBCALL": number,
	        "TIMECALL": number
	      }
	    }
	}
}
```



### HTTP Request 
`***GET*** /accounts/{idacc}/callbyday` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| DateTo | query |  | No | string |
| DateFrom | query |  | No | string |
| limit | query |  | No | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/callbyday` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/CALLBYMONTH
## ***GET*** 

>To authorize and retrieve calls by month, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/callbymonth
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/callbymonth",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/callbymonth",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "datekey": {
	    "month": "string",
	    "year": "string",
	    "NBCALL": 0,
	    "TIMECALL": 0
	  }
	}
}
```

### HTTP Request 
`***GET*** /accounts/{idacc}/callbymonth` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| MonthBack | query |  | No | string |
| idacc | path |  | Yes | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/callbymonth` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/CALLBYMONTHBYNUMBER
## ***GET*** 

>To Authorize and retrieve calls by month, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/callbymonthbynumber
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/callbymonthbynumber",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/callbymonthbynumber",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "datekey": {
	    "month": "string",
	    "year": "string",
	    "numeros": {
	      "idnumber": {
	        "numnumero": number,
	        "supportnumero": "string",
	        "numero": "string",
	        "NBCALL": number,
	        "TIMECALL": number
	      }
	    }
	  }
	}
}
```

### HTTP Request 
`***GET*** /accounts/{idacc}/callbymonthbynumber` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| MonthBack | query |  | No | string |
| idacc | path |  | Yes | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/callbymonthbynumber` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/CALLGEOFRANCE
## ***GET*** 

>To access and get calls with area-code, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/callgeofrance
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/callgeofrance",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/callgeofrance",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "frenchareacode": {
	    "call": 0
	  }
	}
]
```

### HTTP Request 
`***GET*** /accounts/{idacc}/callgeofrance` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| DateTo | query |  | No | string |
| DateFrom | query |  | No | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/callgeofrance` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |


# /ACCOUNTS/{IDACC}/NUMBERS
## ***POST*** 

> To access and add a tracked number to account, use this code 

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/numbers
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "number": "string",
	  "name": "string",
	  "recipientphonenumber": "string",
	  "recipientname": "string"
	}
]
```


### HTTP Request 
`***POST*** /accounts/{idacc}/numbers` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| areacode | query |  | No | string |
| x-api-key | header |  | No | string |
| name | query |  | No | string |
| recipientphonenumber | query |  | No | string |
| country | query |  | No | string |
| numbersAddPost | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/numbers` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/NUMBERS/GETLIST
## ***GET***

> To access available numbers list, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/getlist
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
``` 

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/getlist",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/getlist",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "phonenumber": {
	    "numero": "string",
	    "supportnumero": "string",
	    "formatInternational": "string",
	    "formatNational": "string",
	    "paysNumero": "string",
	    "typeNumero": "string"
	  },
	  "destinataire":{
	    "teldestinataire": "string",
	    "nomdestinataire": "string",
	    "formatInternational": "string",
	    "formatNational": "string",
	    "paysNumero": "string",
	    "typeNumero": "string"
	  }
	},
	...
]
```

### HTTP Request 
`***GET*** /accounts/{idacc}/numbers/getlist` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/numbers/getlist` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/NUMBERS/{PHONENUMBER}/CALLS
## ***GET*** 

> To access and get calls of particular tracked number, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/calls
  -H 'cache-control: no-cache' 
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/calls",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/calls",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "idcall": {
	    "datecall": "string",
	    "heurecall": "string",
	    "timestampcall": number,
	    "callingNumber": "string",
	    "calledNumber": "string",
	    "supportNumero": "string",
	    "duration": number,
	    "typeNumero": "string",
	    "paysNumero": "string"
	  }
	}
]
```

### HTTP Request 
`***GET*** /accounts/{idacc}/numbers/{phonenumber}/calls` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| DateTo | query |  | No | string |
| DateFrom | query |  | No | string |
| limit | query |  | No | string |
| x-api-key | header |  | No | string |
| phonenumber | path |  | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/numbers/{phonenumber}/calls` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/NUMBERS/{PHONENUMBER}/DESTINATION
## ***POST*** 

> To access and get calls of particular tracked number, use this code

```shell
curl -X POST https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/destination
  -H 'cache-control: no-cache' 
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/destination",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/destination",
  "method": "POST",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "number": "string",
	  "previous_recipientphonenumber": "string",
	  "previous_recipientname": "string",
	  "new_recipientphonenumber": "string",
	  "new_recipientname": "string"
	}
]
```

### HTTP Request 
`***POST*** /accounts/{idacc}/numbers/{phonenumber}/destination` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| x-api-key | header |  | No | string |
| name | query |  | No | string |
| recipientphonenumber | query |  | No | string |
| phonenumber | path |  | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/numbers/{phonenumber}/destination` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |


# /ACCOUNTS/{IDACC}/NUMBERS/{PHONENUMBER}/KPI
## ***GET*** 

> To access and get kpi of a phone number, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/1/numbers/0033185088892/kpi
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```
```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/kpi",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/numbers/{phonenumber}/kpi",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "phonenumber": {
	    "call": 0,
	    "time": 0,
	    "lost": 0
	  }
	}
]
```

### HTTP Request 
`***GET*** /accounts/{idacc}/numbers/{phonenumber}/kpi` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| DateTo | query |  | No | string |
| DateFrom | query |  | No | string |
| limit | query |  | No | string |
| x-api-key | header |  | No | string |
| phonenumber | path |  | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/numbers/{phonenumber}/kpi` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/RECIPIENTS
## ***GET*** 

> To access and get recipients of an account, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/recipients
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
    "cache-control": "no-cache"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "recipientphonenumber": {
	    "idrecipient": 0,
	    "name": "string",
	    "recipientphonenumber": "string"
	  }
	}
]
```

### HTTP Request 
`***GET*** /accounts/{idacc}/recipients` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***POST*** 

> To access and add a recipient for an account, use this code

```shell
curl -X POST https://www.magnetis-in.com/v1/accounts/{idacc}/recipients
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients",
  "method": "POST",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "recipientphonenumber": {
	    "idrecipient": 0,
	    "name": "string",
	    "recipientphonenumber": "string"
	  }
	}
]
```

### HTTP Request 
`***POST*** /accounts/{idacc}/recipients` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| phonenumber | query |  | No | string |
| x-api-key | header |  | No | string |
| name | query |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/recipients` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |


# /ACCOUNTS/{IDACC}/RECIPIENTS/{RECIPIENTNUMBER}
## ***OPTIONS*** 

> To access and get details of recipient number, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/recipients/{recipientnumber}
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients/{recipientnumber}",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients/{recipientnumber}",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/recipients/{recipientnumber}` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/RECIPIENTS/{RECIPIENTNUMBER}/TRACKEDNUMBER
## ***GET*** 

> To access and get tracked number of recipient, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/recipients/{recipientnumber}/trackednumber
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients/{recipientnumber}/trackednumber",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/recipients/{recipientnumber}/trackednumber",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

### HTTP Request 
`***GET*** /accounts/{idacc}/recipients/{recipientnumber}/trackednumber` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| recipientnumber | path |  | Yes | string |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/recipients/{recipientnumber}/trackednumber` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /ACCOUNTS/{IDACC}/SEARCH
## ***GET*** 

> To access and get tracked number of recipient, use this code

```shell
curl -X GET https://www.magnetis-in.com/v1/accounts/{idacc}/search
  -H 'cache-control: no-cache'
  -H 'x-api-key: your-magnetis-api-key'
```

```php
$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://www.magnetis-in.com/v1/accounts/{idacc}/search",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "cache-control: no-cache",
    "x-api-key: your-magnetis-api-key"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://www.magnetis-in.com/v1/accounts/{idacc}/search",
  "method": "GET",
  "headers": {
    "x-api-key": "your-magnetis-api-key",
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above code returns JSON structured like this:

```json
[
    {
	  "idcall": {
	    "datecall": "string",
	    "heurecall": "string",
	    "timestampcall": 0,
	    "callingNumber": "string",
	    "calledNumber": "string",
	    "supportNumero": "string",
	    "duration": 0,
	    "typeNumero": "string",
	    "paysNumero": "string"
	  }
	}
]
```

### HTTP Request 
`***GET*** /accounts/{idacc}/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| idacc | path |  | Yes | string |
| DateTo | query |  | No | string |
| DateFrom | query |  | No | string |
| limit | query |  | No | string |
| x-api-key | header |  | No | string |
| callingNumber | query |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

## ***OPTIONS*** 

### HTTP Request 
`***OPTIONS*** /accounts/{idacc}/search` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |

# /TEST
## ***GET*** 

### HTTP Request 
`***GET*** /test` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| x-api-key | header |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | 200 response |