# RC_Mongolian
## 2018-05-15

# RC_Likewu
## 2018-05-08
* [#37](https://github.com/DataBiosphere/firecloud-app/issues/37): When importing data entities from another workspace, the add icon is now always visible and usable. Previously, if you hid all columns, the add icon disappeared, even if you then un-hid individual columns.
* [#52](https://github.com/DataBiosphere/firecloud-app/issues/52): When viewing the details of a genomics operation from a workspace's Monitor tab -> view submission -> view workflow -> show call -> operation, the json for the operation is now pretty-printed for easier reading. Previously it was on a single line, making it difficult to read.
* [#53](https://github.com/DataBiosphere/firecloud-app/issues/53): Upgraded the `hoek` third-party transitive dependency in the UI to address a potential security vulnerability identified as [CVE-2018-3728](https://nvd.nist.gov/vuln/detail/CVE-2018-3728).
* [#58](https://github.com/DataBiosphere/firecloud-app/issues/58): Resolved a JavaScript error that resulted in a blank page when viewing the details of an entity within the Data tab of your workspace, if that entity contained a numeric attribute created via the API. This did not occur for attributes created via TSV upload.

# RC_Koean
## 2018-05-01
* [#8](https://github.com/DataBiosphere/firecloud-app/issues/8): Fixes a bug in the UI's New Relic integration that caused a JavaScript error in the browser and prevented metrics from being delivered to New Relic. This error was invisible to end users unless they had the JavaScript console open and did not impact any other functionality.

# RC_J
## 2018-04-25
* [#3](https://github.com/DataBiosphere/firecloud-app/issues/3): There is now a link to the FireCloud status/uptime dashboard in the footer.

# RC_I
## 2018-04-24
* [#6](https://github.com/DataBiosphere/firecloud-app/issues/6): In the Create Workspace and Clone Workspace modal dialogs, the dropdown of billing projects is now in alphabetical order. Previously, the projects were listed in arbitrary order.
* [#31](https://github.com/DataBiosphere/firecloud-app/issues/31): The Swagger-UI interface at https://api.firecloud.org/ no longer requests OAuth scopes for Google Drive or Google Sheets.

# RC_Hwo
## 2018-04-18
* [#5](https://github.com/DataBiosphere/firecloud-app/issues/5): An email with a plus in it in is now considered valid when in the 'Contact Email for Notifications' field when updating or creating your profile.
* [#29](https://github.com/DataBiosphere/firecloud-app/issues/29): We have resolved a regression from the previous release that caused repeated ajax requests when viewing an individual entity in the Data tab of a workspace. These repeated calls did not impact functionality but did impact performance both in the browser and server-side.
* [#32](https://github.com/DataBiosphere/firecloud-app/issues/32): FireCloud no longer requests the 'View and manage your Google Compute Engine resources' OAuth scope during login.
