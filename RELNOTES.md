# RC_West_of_England
## 2018-07-24

# RC_Vishtines
## 2018-07-17
* [#97](https://github.com/DataBiosphere/firecloud-app/issues/97): Fixed an issue that caused timeouts and errors when attempting to view a workflow that contains many subworkflows.

# RC_Ural
## 2018-07-10
* [#91](https://github.com/DataBiosphere/firecloud-app/issues/91): Improved readability of the error message when adding a non-existent user to a group.
* [#104](https://github.com/DataBiosphere/firecloud-app/issues/104): Fixed a bug that caused an individual workflow's details from displaying, in cases where the system encountered an unexpected error calculating that workflow's cost.

# RC_Twente
## 2018-06-26
* [#80](https://github.com/DataBiosphere/firecloud-app/issues/80): User can now copy the "download metadata" link to increase speed of downloading via command line

# RC_Synthetic
## 2018-06-21
* [#74](https://github.com/DataBiosphere/firecloud-app/issues/74): Updated the swagger-ui response models for the "Monitor submission status" and "Retrieve workflow cost" API endpoints at https://api.firecloud.org/#!/Submissions/monitorSubmission and https://api.firecloud.org/#!/Submissions/workflowCostInSubmission, respectively.
* [#70](https://github.com/DataBiosphere/firecloud-app/issues/70): UX improvements related to call caching, submission and workflow monitoring:
    * Call caching status is now displayed at the submission level and has been removed from the workflow level.
    * Call caching status now accurately reflects the value supplied by the user at submission time. Previously, the call caching value could falsely show as disabled for certain workflows.
    * Hovering over a submission's status column in the Monitor tab now shows the counts of that submission's workflows, grouped by workflow status.
    * When viewing an individual workflow, that workflow's status now shows as both icon and text. Previously it only had an icon.
    * When viewing an individual workflow, that workflow's unexpanded calls now now show their status.
    * When a workflow or a call does not have stdout or stderr logs, the stdout/stderr fields are now hidden. Previously the fields were displayed with a blank value, taking up screen real estate.

# RC_Rung
## 2018-06-12
* No changes in this release.

# RC_Q
## 2018-06-07
* [#76](https://github.com/DataBiosphere/firecloud-app/issues/76): FireCloud has upgraded to Cromwell version 32. For more information on this upgrade, see the official FireCloud release notes for RC_Q at https://software.broadinstitute.org/firecloud/blog?id=12169, and the Cromwell release notes at https://github.com/broadinstitute/cromwell/releases.

# RC_Obroshino
## 2018-05-31
* [#20](https://github.com/DataBiosphere/firecloud-app/issues/20): Actual cloud costs, when available, are now displayed in the details page for individual workflows.
* [#75](https://github.com/DataBiosphere/firecloud-app/issues/75): Fixed an issue where the links to open a GCS bucket were incorrect for certain subworkflows.

# RC_Nungan
## 2018-05-22
* [#11](https://github.com/DataBiosphere/firecloud-app/issues/11): When viewing a single workflow, FireCloud now allows you to drill down into the details of subworkflows.
* [#16](https://github.com/DataBiosphere/firecloud-app/issues/16): When viewing a single submission, FireCloud now shows actual cloud costs for that submission and each workflow in the submission, when available. Cost information will be added to additional parts of the UI in upcoming releases.

# RC_Mongolian
## 2018-05-17
* [#9](https://github.com/DataBiosphere/firecloud-app/issues/9): APIs now better support retrieval of subworkflow metadata and labels. Subworkflow metadata will be exposed in the FireCloud UI in a future release.
* [#12](https://github.com/DataBiosphere/firecloud-app/issues/12): Actual workflow run cost is now returned in the submission status API, when available. This run cost will be exposed in the FireCloud UI in a future release.

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
