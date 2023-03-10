# AffiliateAPI
Parkway Affiliate API
This is the documentation for the Parkway Parking Affiliate Api. You will need to use a Bearer Token which will be provided to you or you can obtain it via the login method.

**Production Endpoint -** https://api.parkwayparking.com/endpoint  
  
**Sandbox Endpoint -** https://sandbox-api.parkwayparking.com/endpoint

## End-point: Parkway Login
Parkway Login method returns a token if the affiliate has API access  
  
email - **Required**  
password - **Required**
### Method: POST
>```
>https://api.parkwayparking.com/endpoint/login
>```
### Headers

|Content-Type|Value|
|---|---|
|Content-Type|application/json|


### Body (**raw**)

```json
{
    "email":"eh@gmail.com",
    "password":"password!!!"
}
```

### Response: 200
```json
{
    "success": true,
    "data": {
        "token": "1|LyuvoCaTDdz7GNr2pqRdDvbVZt3EvrLK3gdmMsde",
        "id": 1,
        "name": "Eric User",
        "email": "eh@gmail.com"
    },
    "message": "User login successful."
}
```

⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get Account Profile
Displays account info
### Method: POST
>```
>https://api.parkwayparking.com/endpoint/me
>```
### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "id": 1,
    "firstname": "Eric",
    "lastname": "User",
    "phone": "9789771212",
    "email": "eh@gmail.com",
    "address": "37 Brighton St",
    "address2": "",
    "city": "Zephyrhills",
    "state": "FL",
    "zip": "33541",
    "country": "US",
    "active": 1,
    "created": "2016-01-31T23:31:06.000000Z"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Get Properties
Fetches a list of properties that belong to the owners account
### Method: GET
>```
>https://api.parkwayparking.com/endpoint/property
>```
### Headers

|Content-Type|Value|
|---|---|
|Content-Type|application/json|


### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": [
        {
            "id": 1,
            "affiliate_id": 1,
            "name": "XYZ Testing, LLC",
            "address": "4510 Pine Hollow Dr",
            "spaces": 22,
            "daily_rate": "5.99",
            "monthly_rate": "151.00",
            "active": 1
        }
    ],
    "message": ""
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Property Details
Fetches a properties details  

**id** - **Required** Property ID (int)
### Method: POST
>```
>https://api.parkwayparking.com/endpoint/property/details
>```
### Body (**raw**)

```json
{"id":1}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": [
        {
            "id": 1,
            "affiliate_id": 1,
            "name": "XYZ Testing, LLC",
            "address": "4510 Pine Way Dr",
            "spaces": 22,
            "daily_rate": "5.99",
            "monthly_rate": "151.00",
            "active": 1
        }
    ],
    "message": ""
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Property Update
Endpoint allows updating Property Spaces and/or the Daily Rate in one request.

**id** - **Required** Property ID (int)  
*Requires one or both params listed below*  
**spaces** - Total Available Spaces for sale (int)  
**daily_rate** - Daily Rate(decimal)
### Method: PUT
>```
>https://api.parkwayparking.com/endpoint/property/update
>```
### Headers

|Content-Type|Value|
|---|---|
|Content-Type|application/json|


### Body (**raw**)

```json
{"id":1,"spaces":22,"daily_rate":7.99}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": {
        "spaces": 22,
        "daily_rate": "7.99",
        "previous": {
            "spaces": 22,
            "daily_rate": "5.99"
        }
    },
    "message": "Property Updated"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Update Property Daily Rate
Allows owner to update the Daily Rate

**id** - **Required** Property ID (int)

**daily_rate** - **Required** Daily Rate (decimal)
### Method: PUT
>```
>https://api.parkwayparking.com/endpoint/property/setdailyrate
>```
### Body (**raw**)

```json
{"id":1,"daily_rate":5.99}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": {
        "id": 1,
        "previous": "7.99",
        "daily_rate": "5.99"
    },
    "message": "Property Updated"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Update Property Space Count
Allows owner to update the Max Available Spaces

**id** - **Required** Property ID (int)

**spaces** - **Required** Total Available Spaces for sale (int)
### Method: PUT
>```
>https://api.parkwayparking.com/endpoint/property/setspaces
>```
### Body (**raw**)

```json
{"id":1,"spaces":10}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": {
        "id": 1,
        "previous": 22,
        "spaces": 10
    },
    "message": "Property Updated"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Property Blackouts
Fetches a properties blackouts

**id** - **Required** Property ID (int)
### Method: POST
>```
>https://api.parkwayparking.com/endpoint/property/blackouts
>```
### Body (**raw**)

```json
{"id":1}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": [
        {
            "id": 1026,
            "property_id": 1,
            "start_date": "2018-11-12 00:00:00",
            "end_date": "2018-11-13 00:00:00",
            "created": "2018-11-12T12:05:20.000000Z",
            "modified": "2018-11-12T12:05:20.000000Z"
        },
        {
            "id": 1583,
            "property_id": 1,
            "start_date": "2019-05-31 00:00:00",
            "end_date": "2019-06-01 00:00:00",
            "created": "2019-05-27T08:36:09.000000Z",
            "modified": "2019-05-27T08:36:09.000000Z"
        },
        {
            "id": 2639,
            "property_id": 1,
            "start_date": "2020-08-28 00:00:00",
            "end_date": "2021-07-31 00:00:00",
            "created": "2020-08-28T10:02:41.000000Z",
            "modified": "2020-08-28T10:02:41.000000Z"
        },
        {
            "id": 3012,
            "property_id": 1,
            "start_date": "2021-05-15 00:00:00",
            "end_date": "2021-05-17 00:00:00",
            "created": "2021-05-11T12:00:33.000000Z",
            "modified": "2021-05-11T12:00:33.000000Z"
        },
        {
            "id": 3013,
            "property_id": 1,
            "start_date": "2021-05-15 00:00:00",
            "end_date": "2021-05-17 00:00:00",
            "created": "2021-05-11T12:04:26.000000Z",
            "modified": "2021-05-11T12:04:26.000000Z"
        },
        {
            "id": 3014,
            "property_id": 1,
            "start_date": "2021-05-16 00:00:00",
            "end_date": "2021-05-18 00:00:00",
            "created": "2021-05-11T12:04:39.000000Z",
            "modified": "2021-05-11T12:04:39.000000Z"
        }
    ],
    "message": ""
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Property Blackout Create
Creates a blackout spanning the start_date and end_date fields. Date Format is "YYYY-MM-DD HH:MM:SS"

**id** - **Required** Property ID (int)  
**start_date** - **Required** Start Date (datetime) "YYYY-MM-DD HH:MM:SS"  
**end_date** - **Required** End Date (datetime) "YYYY-MM-DD HH:MM:SS"
### Method: POST
>```
>https://api.parkwayparking.com/endpoint/property/blackout/create
>```
### Body (**raw**)

```json
{"id":1,"start_date":"2023-12-23 00:00:00","end_date":"2024-01-03 00:00:00"}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": {
        "property_id": 1,
        "start_date": "2023-12-23 00:00:00",
        "end_date": "2024-01-03 00:00:00",
        "modified": "2022-08-06T13:18:21.000000Z",
        "created": "2022-08-06T13:18:21.000000Z",
        "id": 5070
    },
    "message": "Blackout Created"
}
```


⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃ ⁃

## End-point: Property Blackout Remove
Deletes a properties blackout date. Requires a blackout_id from Property Blackouts endpoint

**id** - **Required** Property ID (int)  
**blackout_id** - **Required** Blackout ID (int)
### Method: PUT
>```
>https://api.parkwayparking.com/endpoint/property/blackout/delete
>```
### Body (**raw**)

```json
{"id":1,"blackout_id":1026}
```

### 🔑 Authentication bearer

|Param|value|Type|
|---|---|---|
|token|1|5OAdJD1OeGJKDPiyALElInXeu2N8Ns9MqenLfFze|string|


### Response: 200
```json
{
    "success": true,
    "data": {
        "id": 1,
        "blackout_id": 1026
    },
    "message": ""
}
```
