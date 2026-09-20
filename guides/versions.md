<seotitle>Describe any versions of the API and how to discover the version. 50–60 chars</seotitle>

_> Documenting the versioning strategy that you use for your API product is important. Read the [API Versioning](https://apistyleguide.cisco.com/#!apix-versioning) section of the Cisco API Style Guide to better understand how it can positively (or negatively) impact the developer experience. The [versioning REST-based APIs](https://apistyleguide.cisco.com/#!rest-versioning\) section also provides details._

# API Versions and Backward Compatibility

_> Discuss whether the endpoint contains the API version, what versions are available, any stability or compatibility considerations, and identify any particular methods or API services considered experimental. Meraki example:_

The Meraki OpenAPI spec, is THE SOURCE OF TRUTH, defining the publicly supported state of the Dashboard API.

Once we release a major API version, we make only backwards-compatible (minor) changes to it.

These changes include:

* Adding new API resources
* Adding new optional request parameters to existing API methods
* Adding new properties to existing API responses
* Changing the order of properties in existing API responses

_> If there is a particular header to send with a request to access experimental versions, let users know. SD-WAN example:_

vManage API adopts common practices of lifecycle management. Client can use an HTTP media content header to
specify the API version it expects to accept. Service uses HTTP custom header to indicate the version
and current stability of the API.

HTTP accept media type format is: `Accept: application/vnd.cisco.{major_version.minor_version}+json`.
HTTP custom header from service is: `X-Version: {major_version.minor_version};{state}`, the state can
be one of the "prerelease", "release", "deprecate".

If no accept media type indicator in API request, it defaults to version 1.0. Same for the X-Version
response header.

_> Additional resources and Cisco product examples:_

* [SD-WAN versioning docs](https://developer.cisco.com/docs/sdwan/#!api-versions)
* [Meraki versioning and sunset docs](https://developer.cisco.com/meraki/api/#!versioning/v0-deprecation--sunset)


