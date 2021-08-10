# Getir Assignment

This application is build with Node.js and MongoDB. The endpoint fetches the records from DB.

## Prerequisites
* [Node.js](https://nodejs.org/en/)
* [MongoDB](https://www.mongodb.com/)

## Endpoints
```
localhost:3000/records/fetch
```

## Installation

### POST records/fetch

> Success
```
{
    "startDate": "2016-01-26",
    "endDate": "2018-02-02",
    "minCount": 2000,
    "maxCount": 2300
}
```

```
{
    "code": 0,
    "msg": "Success",
    "records": [
        {
            "key": "ORqgjoiv",
            "createdAt": "2016-10-20T18:05:23.890Z",
            "totalCount": 2003
        }
    ]
}
```

> Invalid
```
{
    "startDate": "15-01-2015",
    "endDate": "2018-02-02",
    "minCount": 2000,
    "maxCount": 2300
}
```

```
{
    "msg": "Invalid request",
    "code": 1,
    "errors": [
        "Start Date Format should be 'YYYY-MM-DD'"
    ]
}
```

## To run application in local
1. Create .env file 
``` 
PROD_URI = 'Insert Production URI'
TEST_URI = 'Insert test URI' 
```

2. Install packages ``` npm install ```

3. Run using Nodemon ``` npm start-dev ```

4. Run test cases ``` npm run test ```
