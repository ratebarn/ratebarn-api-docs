# ratebarn-api-docs

API Documentation


## Manage Access Tokens

To manage access tokens, login to gosavvy.io using the GoSavvy user account. Navigate to "Account Settings", Then navigate to "Developer Console". Using the Developer Console you can create and manage existing access tokens. 

#### Create Access Tokens
To create a new accces token token, click "Create new token". Give the token a name and click "Create". Now copy/save the generated access token in a secure place.      


#### Passing Access Token

Pass the access token using the "Authorization" header.

```bash
curl -X GET \
  https://gosavvy.io/api/v1/quote_requests \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {**YOUR-ACCESS-TOKEN**}' \
  -d ''
```