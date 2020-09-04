# ratebarn-api-docs

API Documentation

*FOR HELP & SUPPORT CONTACT: support@gosavvy.io*

- *Show quote request* [get-quote-request](https://github.com/ratebarn/ratebarn-api-docs/blob/master/resource-get-quote-request.md)
- *List quote requests* [get-quote-requests](https://github.com/ratebarn/ratebarn-api-docs/blob/master/resource-get-quote-requests.md)
- *Create quote request* [post-quote-requests](https://github.com/ratebarn/ratebarn-api-docs/blob/master/resource-post-quote-requests.md)

## Manage Access Tokens

To manage access tokens, login to gosavvy.io using the GoSavvy user account. Navigate to "Account Settings", Then navigate to "Developer Console". Using the Developer Console you can create and manage existing access tokens. 

#### Create Access Tokens
To create a new access token token, click "Create new token". Give the token a name and click "Create". Now copy/save the generated access token in a secure place.      

[Create new access token]: .assets/screenshots/create-access-token.png "Create new access token"

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
