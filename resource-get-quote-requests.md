#### Create Quote Request 
```
POST /api/v1/quote_requests
```

*Stores new quote request model, returns saved model*

###### Parameters
The paramters are all passed in the body as a json object. The exact format of this data is best found in the example below. 

Some attributes are expected in a specific format:

| Attribute | Format |
| --- | --- |
| Phone Numbers | 999999999 |
| Dates | YYYY-MM-DD |
| State | two-character abbreviation |
| Currencies | integer value only |


Some attributes accept a value which is from a fixed list of values:

| Attribute | Acceptable Values |
| --------- | ----- |
| gender | Male, Female |
| coverage | Standard, Premium |
| marital_status | Married, Single, Divorced, Widowed, Engaged, Married but Separated |
| home_type | New Home, Refinancing, Shopping Around |
| ownership | Single Family, Condo/Townhouse |
| property_classification | Primary Residence, Vacation Home, Investment Property |
| subscription | true,false |
| terms | true,false |
| coverage_type | Interior & Exterior (HO‌-3), Interior Only (HO‌-6), Unsure |


###### Required Fields
The required attributes are as follows.


| Attribute | Data Type |
| --------- | --------- |
| first_name | required/string/max:255 |
| last_name | required/string/max:255 |
| phone | required/string/max:9 |
| email | required/string/email format |
| birth_date | nullable/string, date format |
| spouse_birth_date | nullable/string, date format |
| cosigner_birth_date | nullable/string, date format |
| terms | string `Y` |
| coverage | string (from list) |
| marital_status | nullable/string (from ['Married', 'Single','Widowed','Divorced','Engaged','Separated']) |
| address | object |
| homes | array of objects |
| subscription | boolean |
| gender | nullable/string (from ['Male','Female']) |



###### Example

```bash
curl -X POST \
  https://www.ratebarn.com/api/v1/quote_requests \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {**YOUR-ACCESS-TOKEN**}' \
  -d '{
          "first_name": "John",
          "last_name": "Doez",
          "gender": "Male",
          "phone": "2221113333",
          "primary_birthday": "1974-01-22",
          "email": "support@gosavvy.io",
          "coverage": "Standard",
          "marital_status": "Married",
          "address": {
            "address_line_1": "111 Anyplace Ave",
            "address_line_2": "Apartment #22",
            "city": "Detroit",
            "state": "MI",
            "zip_code": "48089"
          },
          "homes": [{
              "home_type": "New Home",
              "ownership": "Single Family",
              "coverage_type": "Interior & Exterior (HO‌-3)",
              "property_classification": "Primary Residence",
              "address": {
                "address_line_1": "111 Anyplace Ave",
                "address_line_2": "Apartment #22",
                "city": "Detroit",
                "state": "MI",
                "zip_code": "48089"
              },
          }],
          "drivers": [{
              "first_name": "John",
              "last_name": "Doez",
              "birth_date": "2016-01-05",
              "license_no": "0002214444",
          },{
              "first_name": "Joan",
              "last_name": "Doez",
              "birth_date": "2000-01-05",
              "license_no": "0001114444",
          }],
          "spouse_first_name": "Arlo",
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
          "estimated_loan_amount": 901528,
          "homeowner_claims": false,         
          "subscription": true,
          "terms": true,        
          "notes": "Iure deleniti cupiditate.",          
        }'
```

###### Response
```javascript
{
    "message": "Quote request created!"
    "quote_request_id": 2697
}
```
