# Authentication

_> This page is necessary. Do not delete._ 

_>It is important to design a consistent authentication and authorization approach for your API. This page documents the overall flow and serves as an important reference for developers looking to integrate your API. The ["Authentication and Authorization"](https://developer.cisco.com/api-guidelines/rest-auth/\) section of the Cisco API Guidelines provides recommendations for authentication and authorization decisions. It also discusses other factors to consider, such as the expiration of access tokens and refresh tokens._

_> The first thing a newcomer wants to know is what operations require authorization and what is possible with an API with proper credentials._ _Example from Catalyst Center and Meraki:_

The XYZ Dashboard API requires access via an authenticated and authorized account. Only authorized accounts are able to submit requests to API operations. All operations must communicate over a secure HTTPS connection.

_> Expand on how to provide the API key, API token, or other credentials (usually in a header or as a token request). Provide clean, stepwise information for authenticating to use the API. Include screenshots if there is a dashboard to generate an API key or token._

When a user authenticates, they receive an authorization token to include in the request of each API operation. TProvide the API token on every request using the `Authorization` request header with a value of `Bearer <api token>`. For example:

```
...example goes here...
```

_> If any policies or role-based access controls are in place, describe those here._

To interact with API resources, you need the following scopes:

| Scope                           | Description                        |
|---------------------------------|------------------------------------|
| dashboard:device_read           | Retrieve a device owned by you.    |
| dashboard:device_write          | Create, manage, or remove a device.|
| ...                             | ...                                |

_> Additional resources and Cisco product examples:_

* [Cisco XDR Authentication](https://developer.cisco.com/docs/cisco-xdr/authentication/)
* [Cisco Catalyst Center Authentication](https://developer.cisco.com/docs/dna-center/#!authentication-and-authorization/environment)
* [Meraki Authentication](https://developer.cisco.com/meraki/api-v1/authorization/)
* [Webex Meetings Authorization](https://developer.webex.com/docs/api/getting-started)
