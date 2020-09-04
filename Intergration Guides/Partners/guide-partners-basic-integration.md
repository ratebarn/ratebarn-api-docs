#### Guides - Partners Basic Integration

### Summary

Follow this guide to setup a complete workflow to referer your customer to Savvy via the Savvy API, customers will receive quotes, select quotes and bind with insurnace agency, you will then receive the Dec Page/Inovice.

### Guide

#### Start new quote request
Use the POST quote requests method to send a new customer to Savvy
 - See [resource-post-quote-requests](../../resource-post-quote-requests.md)
 
The API JSON response will include a web link for customers to view quote request status and compare/select quotes when available. 
 
###### Example OST quote requests API Response
 ```json
{
  "data": {
    "id": 3478,
    "quotes_link": "https:\/\/gosavvy.io\/quotes\/3478",
    "status": "open"
  }
}
```
 - SEE ALL RETURN FIELDS [resource-post-quote-requests](../../resource-post-quote-requests.md)
 
 ```data.quotes_link```
#### Display or redirect users to web link 
Next, embed or redirect users to the "quotes_link" so customer can make final selection.
 
###### Example 
 ```html
<a href="{{ apiResponse.data.quotes_link }}">View quotes</a>
```

You can also retrieve and select the quotes via the API see Next steps/Advanced guides. 
 
### Next steps

###### View quote_request and quote request quotes via the API

Use the GET quote requests method to view quote request and quotes on file
 - See [resource-get-quote-requests](../../resource-get-quote-requests.md)

Alternate you can request just the quotes by using the GET quote reqquests quotes method.
 - See [resource-get-quote-request-quotes](../../resource-get-quote-request-quotes.md)


#### Advanced 
  - See Partner Guide Advanced Integration [guide-partners-advanced-integration](guide-partners-advanced-integration.md)
  
 