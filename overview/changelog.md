# API Changelog 

_> This page is necessary. Do not delete. Even a new API must have a changelog that includes a version number and release date._ 

_> Document new revisions including nonbreaking changes on this page. See [Changelog and release notes](https://developer.cisco.com/api-guidelines/apix-versioning/#api-changelog) in the API Guidelines for more information._

_> The version number should follow the semantic versioning specifications using 'MAJOR.MINOR.PATCH'._

_> Replace this file with a generated Changelog from [API Insights](https://developer.cisco.com/docs/api-insights-internal/introduction/#api-insights-for-cisco-engineering-groups) or manually create the Changelog based on the following template._

_> Organize the releases in descending order with the most recent release at the top of the page. For each release, include the version number and date, and group changes under subheadings: Breaking Changes, New, Deprecated, and Updates. Within each subheading, further organize the changes by tag name._



_> Example for a new API: 

```
## Version 1.0
### v1.0.0 - YYYY-MM-DD
Initial release of the XYZ API.
```
  
_> Example for a prereleased API: 

```
## Version 0.1
### v0.1.0-Rev.1 - YYYY-MM-DD
Initial release of the XYZ API in Early Field Trial (EFT). Please note that features may change and are not guaranteed to maintain backwards compatibility. 
```

_> Example for an updated API:

```
## Version X.Y
### vX.Y.Z - YYYY-MM-DD

#### Breaking Changes

[Alarm]
- POST /xyz/appcenter/alarm
  - Added the new required request property 'getAlarmId'

#### New

[Alarm]
- POST /xyz/appcenter/alarm/status
  - New operation

#### Deprecated
The following operations and properties will be removed in future releases. Therefore, it is not recommended to use these resources.

[License]
- POST /xyz/appcenter/license
  - Deprecated operation

#### Updates

[Alarm]
- GET /xyz/appcenter/alarm
  - Added the new optional 'query' request parameter
```
