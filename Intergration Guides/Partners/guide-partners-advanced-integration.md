#### Guides - Partners Advanced Integration

##### Step 1 - Creating a lead

1. Store new quote quest
    1. Display to your users a form to collect this information or pass existing stored information 
    2. Pass data as a JSON object to the Quote Request POST API method.
        1. 
        example: 
        ```json
        {
          "data": {
            "id": 3478,
            "quotes_link": "https:\/\/gosavvy.io\/quotes\/3478",
            "status": "open"
          }
        }
       ```
    3. Save  Quote Request ID from returned Quote Request API Response. 

##### Step 2 - Displaying Quotes

1. Get quote request.
    1. Use the Quote Request GET API method using the Quote Request ID
    2. Determine if from Quote Request API Response if field ```status``` is set to value 
    "quoted". if so move to next step. if not show a UI to your users that quotes are still pending.
2. Get quote request's quotes.
    1. Use the Quote Request Quotes GET API method to pull the quotes using the Quote Request ID
3. Display quotes to your end users.

##### Step 2.B - Add bundle auto to an existing Quote Request.

1. Display a form to collect information about Drivers and Vehicles information
    1. See Vehicle Makes API and Vehicle Model API to make sure to send the correct ```vehicle_make_id``` and ```vehicle_model_id``` when creating or updating Quote Request's vehicles.
    2. Use the Quote Request PUT method to update the Quote Request.
    3. After bundle auto is been set after quote request field ```status``` will be changed to 'pending'.
    
##### Step 3 - Choose quote

1. Set quote to chosen
    1. Use the Quote Request Quote PUT method to update quote to set field ```chosen``` to *TRUE*
    2. Use the Quote Request Quotes GET API method to get newly updated quote request data.
    3. Agency contact information will be available in the ```chosen_quote``` property of the Quote Request API response.       
    

### Still need help?

If you need help please contact support 

- Contact support
    - Email: [support@gosavvy.io](support@gosavvy.io)