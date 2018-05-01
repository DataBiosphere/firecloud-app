# RC_Koean
## 2018-05-21
* nothing to note in this release.

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
