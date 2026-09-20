<seotitle>Top keywords about errors and troubleshooting your API, 50–60 chars</seotitle>

# Errors and Troubleshooting

_> Provide information on how to find logs that give more information about API errors. Also be sure to list all possible HTTP status errors in one place, in addition to providing possible errors for each API call. Below are Meraki examples:_

Error responses from the API generally use standard HTTP status codes. Some examples:

| Status Code  | Status Message        | Meaning                                |
|--------------|-----------------------|----------------------------------------|
| 200          | OK                    | All looks good                         |
| 201          | Created               | New resource created                   |
| 400          | Bad Request           | Request was invalid                    |
| 401          | Unauthorized          | Authentication missing or incorrect    |
| 403          | Forbidden             | The request was understood but not     |
|              |                       |  allowed.                              |
| 404          | Not Found             | Resource not found                     |
| 500          | Internal Server Error | Something wrong with the server        |
| 503          | Service Unavailable   | Server is unable to complete request   |

If the response code isn't specific enough to identify the issue's cause, the response will include error messages in JSON format, for example:

... example JSON snippet ...

# Error Handling

The API raises exceptions in the event something failed, such as missing or invalid parameters.
We recommend writing code that gracefully handles all possible API exceptions.

... examples using Python, other languages as appropriate ...

_> Additional resources and Cisco product examples:_

* [Meraki Guides: Errors and Troubleshooting](https://developer.cisco.com/meraki/api-v1/#!errors)
