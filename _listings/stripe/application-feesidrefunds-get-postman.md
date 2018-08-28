{
  "info": {
    "name": "Stripe Get Application Fees  Refunds",
    "_postman_id": "1204dabb-8878-4359-8f7a-1cbe0ed8f06f",
    "description": "You can see a list of the refunds belonging to a specific application fee. Note that the 10 most recent refunds are always available by default on the application fee object. If you need more than those 10, you can use this API method and the limit and starting_after parameters to page through additional refunds.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "application",
      "item": [
        {
          "id": "c0eb5e2f-937b-4030-8361-1c7972f5bfaf",
          "name": "getApplicationFeesRefunds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stripe.com",
              "path": [
                "v1",
                "application_fees/:id/refunds"
              ],
              "query": [
                {
                  "key": "ending_before",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "starting_after",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "You can see a list of the refunds belonging to a specific application fee"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "353cdaa0-e025-4fc4-8642-ac1915ce4a67"
            }
          ]
        }
      ]
    }
  ]
}