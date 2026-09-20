<seotitle>Top keywords about results, data sets and how to page through results, 50-60 chars</seotitle>

_> Most APIs offer some kind of sorting, filtering, and pagination support. A dedicated guide helps developers accelerate their understanding and apply better practices in this area._

_> Below are some example headings and sample content to help get started. Adjust as needed to fit the needs of your API and its target developers._

# Browsing Returned Results

_> Be clear about the maximum and minimum number of results you will return. You may also want to discuss rate limits here._

Generally, API pagination relies on a snapshot of data at the time you invoke the API operation. There is no guarantee of data consistency between different API invocations.

# Understanding Pagination

_> Inform the user of response limits, result count, accessing the next page, and recognizing the end of the list._

Paginated GET endpoints only return a subset of the results in the first response. Use the following query arguments to shape paginated results:

* ...
* ...
* ...

# Sorting Results

_> Describe whether you can query or filter your results using certain methods. Also mention if some or all list/browse operations do not support sorting._

Currently sorting is only available for device stats and statistics APIs. Use the following query arguments to control sorting:

* ...
* ...
* ...

# Filtering Results

_> Describe if your results can be queried or filtered by certain methods._

Filtering varies for each list/browse operation, using the following query arguments:

* ...
* ...
* ...

# Rate Limits on Results

_> Describe what rate limits are in place, and if there is any way to request or set higher or lower rate limits._

## Per Organization

Default rate limits apply as follows:

* ...
* ...
* ...

## Response Codes

Use the following response code to indicate if a rate limit is exceeded:

* Return a 429 status code with the Retry-After header when the rate limit is exceeded.

When an application surpasses the rate limit, the response body will include the following message:

...


_> Additional resources and Cisco product examples:_

* [SD-WAN Guides: Understanding Pagination](https://developer.cisco.com/docs/sdwan/#!browsing-returned-results-sorting-results-filtering-results-and-rate-limits/understanding-pagination)
* [Meraki Guides: Pagination](https://developer.cisco.com/meraki/api-v1/#!pagination/how-does-pagination-work-in-the-dashboard-api)
* [Meraki Guides: Rate Limits](https://developer.cisco.com/meraki/api-v1/#!rate-limit)
