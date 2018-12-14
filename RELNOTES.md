# RC_Knabstrupper
## 2018-12-19
### Fixes
* [#227](https://github.com/DataBiosphere/firecloud-app/issues/227) Fixed a bug that prevented the viewing of an individual workflow, if the current workspace had a space in its name. This bug was introduced in the November 14, 2018 release. Thanks to @mbookman for identifying this bug.
* [#234](https://github.com/DataBiosphere/firecloud-app/issues/234) The workflow timing diagram now shows a tooltip of "Running" for properly-running tasks. Previously, it incorrectly showed "Still Running when workflow ended" even though the workflow had not ended. This bug was introduced in the November 1, 2018 release.
### Infrastructure
* [#223](https://github.com/DataBiosphere/firecloud-app/issues/223) To improve security, the FireCloud UI now incorporates protection from the [tCell](https://www.tcell.io/how-it-works/features-protections/browser-protection/) browser agent.


# RC_JejuHorse
## 2018-11-29
* [#83](https://github.com/DataBiosphere/firecloud-app/issues/83) Improved an error message. Previously, users would see a message `sendReceive doesn't support chunked responses, try sendTo instead`, which was unhelpful and confusing. Now, this error better indicates what's really happening: `The response payload was over 20MB and cannot be processed.`
* [#136](https://github.com/DataBiosphere/firecloud-app/issues/136) The warning banner that states "Your offline credentials are missing or out-of-date..." is now bright red instead of yellow, in an attempt to make it more obvious. Additionally, new users who accept the Free Credits offer will see their browsers fully refresh after accepting, in order to reload all their cached data.
* [#206](https://github.com/DataBiosphere/firecloud-app/issues/206) When viewing a single workflow's details, the FireCloud UI now defers its cost calculation until after it renders the workflow details. Since cost calculation can be slow, this allows the UI to serve the workflow details faster.
* [#213](https://github.com/DataBiosphere/firecloud-app/issues/213) The FireCloud UI now requests a smaller, streamlined payload from the API when rendering workflow details. This allows the UI to serve the workflow details faster and eliminates some - but not all - errors caused when the workflow details API response is too large.
* [#214](https://github.com/DataBiosphere/firecloud-app/issues/214) The FireCloud UI now only requests the data to populate a workflow's timing diagram on demand, once a user clicks to show the diagram. Previously the UI loaded this data when the page first rendered. This further allows the UI to serve the workflow details faster and eliminates some - but not all - errors caused when the workflow details API response is too large.
* [#218](https://github.com/DataBiosphere/firecloud-app/issues/218) The FireCloud UI now shows an error message in certain situations on the workspace list and the submission list within a workspace. Previously, the error message was suppressed and, in the case of a backend error, the UI rendered an empty page.

# RC_IrishHunter
## 2018-11-14
* [#111](https://github.com/DataBiosphere/firecloud-app/issues/111) The FireCloud UI now has links in a few places for improved usability: 
    * when viewing the list of method configurations in a workspace, the name of the referenced method is now a link.
    * when viewing a single method configuration in a workspace, the snapshot id now links to the referenced method.
    * when viewing a submission, the method configuration name is now a link.
* [#212](https://github.com/DataBiosphere/firecloud-app/issues/212) The API to get call-level metadata for a workflow now supports query parameters to control which fields should be returned in the response. This is particularly useful for querying specific data about a workflow where the full response is otherwise very large. Cromwell has offered this functionality for multiple releases but it has not been exposed via the FireCloud API. See the Swagger documentation for specifics.
* [#217](https://github.com/DataBiosphere/firecloud-app/issues/217) The login process now eliminates an unnecessary Ajax request for the Terms of Service content. Users may see a very slight incremental performance improvement during login.

# RC_Heck
## 2018-10-30
* [#42](https://github.com/DataBiosphere/firecloud-app/issues/42): To continue ensuring a secure platform, FireCloud now requires users to actively accept the FireCloud Terms of Service prior to using the platform. These Terms of Service will be displayed once a user logs-into FireCloud. A user will be unable to work in FireCloud until these Terms of Service are accepted.
* [#208](https://github.com/DataBiosphere/firecloud-app/issues/208): The workflow timing diagram inside the Monitor tab of a workspace has been updated for stability. Additionally, where previously the diagram displayed "myworkflow.mycall" for each row, it now displays only "mycall" to save space.

# RC_Galiceno
## 2018-10-23
* [#122](https://github.com/DataBiosphere/firecloud-app/issues/122): The Data tab of workspaces is now resilient to unknown entity attribute names listed in a `workspace-column-defaults` workspace attribute.

# RC_EastFriesian
## 2018-10-09
_no changes in this release_

# RC_DanubeDelta
## 2018-10-02
* [#67](https://github.com/DataBiosphere/firecloud-app/issues/67): FireCloud now shows a more helpful error message if you manually load a nonexistent method in the Method Repository - for instance, if you had a browser bookmark that is no longer valid.
* [#127](https://github.com/DataBiosphere/firecloud-app/issues/127): The help link in the "Import Metadata" modal of a workspace now links directly to the relevant page of the user guide, instead of linking to the user guide's homepage.
* [#134](https://github.com/DataBiosphere/firecloud-app/issues/134): When viewing FireCloud in a small-width browser window, the secondary navigation tabs inside a workspace now wrap instead of extending off the screen.

# RC_CarolinaMarshTacky
## 2018-09-25
* [#191](https://github.com/DataBiosphere/firecloud-app/issues/191): Removed an infinite spinner triggered by attempting to preview a DOS object, if that DOS object resolved to a text file or log file.
* [#168](https://github.com/DataBiosphere/firecloud-app/issues/168): Fixed an error caused by attempting to populate a method configuration with a json file larger than 4kb.

# RC_BlackForestColdBlood
## 2018-09-18
* [#170](https://github.com/DataBiosphere/firecloud-app/issues/170): Upgraded IGV.js from v1.0.6 to v2.0.0-rc5 in the Analysis tab of a workspace. For more information on IGV.js and IGV in general, see https://github.com/igvteam/igv.js and https://software.broadinstitute.org/software/igv/.


# RC_AmericanCreamDraft
## 2018-09-12
* [#156](https://github.com/DataBiosphere/firecloud-app/issues/156): Workspace readers no longer see the "Abort" button for running submissions. This button was previously visible to users with read-only workspace access, even though it did not allow those users to successfully abort a submission.

# RC_Zatory
## 2018-08-21
* [#24](https://github.com/DataBiosphere/firecloud-app/issues/24): Improved performance and stability in uncommon cases when reading from the entity data model, if the data model has extremely wide or long attributes.
* [#114](https://github.com/DataBiosphere/firecloud-app/issues/114): Improved the UX for the NPS survey for new users. Users who have already responded to the survey will not see the survey again.
* [#157](https://github.com/DataBiosphere/firecloud-app/issues/157): Squashed a rarely-occurring bug that caused errors when viewing individual workflows, if those workflows had no immediate calls/tasks

# RC_Yong_Kang_Grey
## 2018-08-09
* [#34](https://github.com/DataBiosphere/firecloud-app/issues/34): FireCloud will now remember the list of email addresses with whom you share workspaces and offer those emails as autocomplete suggestions in the sharing dialog. This feature tracks your shares going forward, but cannot not reach backwards into history to suggest shares you've made in the past.
* [#105](https://github.com/DataBiosphere/firecloud-app/issues/105): Tweaked the sort order when sorting submissions by the Status column. Similar statuses now sort next to each other; previously sorting was purely alphabetical.

# RC_Xupu
## 2018-07-31
* [#61](https://github.com/DataBiosphere/firecloud-app/issues/61): FireCloud no longer tracks user behaviors in Google Analytics.
* [#113](https://github.com/DataBiosphere/firecloud-app/issues/113): Upgraded to Cromwell 34 inside FireCloud. For more information on Cromwell 34, see the Cromwell release notes and official FireCloud release notes.
* [#133](https://github.com/DataBiosphere/firecloud-app/issues/133): Minor performance improvement via reducing unnecessary ajax requests when switching tabs inside a workspace.
* [#137](https://github.com/DataBiosphere/firecloud-app/issues/137): Performance improvement via caching of WDL validation. Users may notice improved performance when viewing a method configuration inside a workspace.

# RC_West_of_England
## 2018-07-24
* [#33](https://github.com/DataBiosphere/firecloud-app/issues/33): FireCloud no longer requires the OAuth scope to "Manage your data and permissions in Google Cloud Storage" when logging in.
* [#110](https://github.com/DataBiosphere/firecloud-app/issues/110): Selecting and copying gs:// and dos:// urls from within the FireCloud UI no longer copies extraneous unprintable/invisible characters.


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
