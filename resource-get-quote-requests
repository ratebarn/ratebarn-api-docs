#### Create Quote Request 
```
POST /api/v1/quote_requests
```

###### Parameters
The paramters are all passed in the body as a json object. The exact format of this data is best found in the example below. 

Some attributes are expected in a specific format:

| Attribute | Format |
| --- | --- |
| Phone Numbers | 9999999999 |
| Dates | YYYY-MM-DD |
| State | two-character abbreviation |
| Currencies | integer value only |


Some attributes accept a value which is from a fixed list of values:

| Attribute | Acceptable Values |
| --------- | ----- |
| gender | Male, Female |
| coverage | Standard, Premium |
| marital_status | - Married, Single, Divorced, Widowed, Engaged, Married but Separated |
| home_type | New Home, Refinancing, Shopping Around |
| ownership | Single Family, Condo/Townhouse |
| property_classification | Primary Residence, Vacation Home, Investment Property |
| subscription | Y |
| terms | Y |
| coverage_type | Interior & Exterior (HO‌-3), Interior Only (HO‌-6), Unsure |


###### Required Fields
The required attributes are as follows.


| Attribute | Data Type |
| --------- | --------- |
| first_name | string |
| last_name | string |
| phone_number | string |
| primary_birthday | string, date format |
| terms | string `Y` |
| email | string, email format |
| coverage | string (from list) |
| marital_status | string (from list) |
| address_attributes | object |
| subscription | string `Y` |
| gender | string (from list) |


###### Partner Email Attribute
Because most automated requests will be sent using an automation/service partner account, the submitting partner may provide a separate email address as part of the request in the `partner_email` attribute of the `quote_request`. This email will be included in partner emails realated to the submitted quote request.


###### Example

```bash
curl -X POST \
  https://www.ratebarn.com/api/v1/quote_requests \
  -H 'Content-Type: application/json' \
  -H 'X-Partner-Email: you@yourcompany.com' \
  -H 'X-Partner-Token: your_api_key' \
  -d '{
        "quote_request": {
          "first_name": "August",
          "last_name": "Hane",
          "gender": "Male",
          "phone_number": "2125551214",
          "primary_birthday": "1974-05-21",
          "email": "Flo_Stracke53@yahoo.com",
          "coverage": "Standard",
          "marital_status": "Married",
          "address_attributes": {
            "street_address": "111 Anyplace Ave",
            "city": "Anyplace",
            "state": "IL",
            "zip_code": "66666"
          },
          "spouse_name": "Arlo",
          "spouse_last_name": "Balistreri",
          "spouse_birthday": "1956-05-22",
          "mortgagee_clause": "Placeat totam ratione.",
          "cosigner": true,
          "cosigner_first_name": "Noe",
          "cosigner_last_name": "Dietrich",
          "cosigner_birthday": "2001-05-14",
          "loan_number": "96169211",
          "current_insurer": "Acuity",
          "current_insurance_price": 1574,
          "closing_date": "2019-12-25",
          "notes": "Iure deleniti cupiditate.",
          "homeowner_claims": false,
          "estimated_loan_amount": 901528,
          "subscription": "Y",
          "terms": "Y",
          "homes_attributes": [{
              "home_type": "New Home",
              "ownership": "Single Family",
              "coverage_type": "Interior & Exterior (HO‌-3)",
              "property_classification": "Primary Residence",
              "address_attributes": {
                "street_address": "48074 Lebsack Spurs",
                "city": "Ulicesberg",
                "state": "IL",
                "zip_code": "60606"
              }
          }]
        }
      }'
```

###### Response
```javascript
{
    "message": "Quote request created!"
    "quote_request_id": 2697
}
```
