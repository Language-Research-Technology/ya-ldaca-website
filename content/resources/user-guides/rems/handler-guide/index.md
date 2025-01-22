---
title: "REMS Handler Guide"
date: 2025-01-17T09:26:32+11:00
draft: false
description: "A guide for the options and tasks available in LDaCA REMS to users with the Handler role."
---

<br>

##### [Process License Applications](#process-license-applications)

##### [Revoke Entitlements](#revoke-entitlements)

##### [Manage the Deny List](#manage-the-deny-list)

<br>

Resource Owners assign users (including themselves) as Handlers during [Workflow creation](../owner-guide/#51-create-a-workflow).

> For each role you have in LDaCA REMS, log in with a consistent identity provider as all your actions are connected to your login identity.

<br>

## Process License Applications

<br>

### Email notifications

Handlers receive email notifications about new applications for the resource they are assigned to. If the Resource Owner is not also assigned as Handler, they will not receive notifications about applications.

<br>

### Process a New Application

- View the email notifying about a new license application (example below):

{{< image Src="/user-guides/rems/REMS-NewLicenseApplicationEmail.png" Alt="REMS New License Application Email" Desc="REMS New License Application Email" Title="REMS New License Application Email" Ref="LDaCA" >}}

<br>

- Click on the link in the email - it directs to the LDaCA REMS login page (if you were not already logged in) and opens the specified application form.
- The applications you have handled are listed in the **_Actions_** menu
- Locate the application record you'd like to review from the **_Actions_** list (categorised into either Open Applications or Processed Application)
- Click the **_View_** button in the relevant row
- In the Application record, in the _State_ section, click **_Show more_** to display application details and _Events_ where the history of actions are recorded.

{{< image Src="/user-guides/rems/Handler-CheckEvents.png" Alt="REMS Application Record with Events Record" Desc="REMS Application Record with Events Record" Title="REMS Application Record with Events Record" Ref="LDaCA" >}}

<br>

### Actions Available from the Application Form

- In the _Actions_ section (right-hand side) are the following options:

{{< image Src="/user-guides/rems/Handler-AllActions.png" Alt="REMS Application Form Actions" Desc="REMS Application Form Actions" Title="REMS Application Form Actions" Ref="LDaCA" >}}

<br>

#### Approve or reject

- Select this option to approve or reject an application. A _Comment_ text field, **_Upload an attachment_** button and **_Date for access rights to expire_** field for entitlement expiration date are available.
  > It is important to document the reason(s) for the approval or rejection. Provide this information and other pertinent details in the _Comment_ text field. The information provided will be saved and be available only from the application record - visible to the Resource Owner, Handler and Applicant. Comments are not sent via the standard email notifications.
- The Applicant will need to log in to LDaCA REMS to view the comments and any uploaded material.

{{< image Src="/user-guides/rems/Handler-ApproveOrRejectWindow.png" Alt="REMS Application Approve or Reject" Desc="REMS Application Approve or Reject" Title="REMS Application Approve or Reject" Ref="LDaCA" >}}

<br>

- Rejecting an application notifies the Applicant of this decision but does not automatically put the Applicant on the Deny List which means they can apply again. (Revoking entitlements puts the Applicant on the Deny List for the relevant resource).

<br>

#### Return to Applicant

- This option allows the application to be amended, e.g. by obtaining more information from the Applicant. The Applicant can resubmit the application.

{{< image Src="/user-guides/rems/Handler-ReturnToApplicant.png" Alt="REMS Application Return to Applicant" Desc="REMS Application Return to Applicant" Title="REMS Application Return to Applicant" Ref="LDaCA" >}}

<br>

- A _Comment_ text field and an **_Upload_** button are available.
  > It is important to document the reason for returning the application and what is required of the Applicant – provide this information and related details in the _Comment_ text field. The information provided will be saved and be available only from the application record. Comments are not sent via the standard email notifications.
- The Applicant will need to log in to LDaCA REMS to view the comments and any uploaded material.

<br>

#### Request review

- Select this to notify the designated Reviewer (e.g. the organisation Owner in LDaCA REMS, who may also be the data steward) that the application needs to be reviewed.

{{< image Src="/user-guides/rems/Handler-RequestReview.png" Alt="REMS Application Request Review" Desc="REMS Application Request Review" Title="REMS Application Request Review" Ref="LDaCA" >}}

<br>

{{< image Src="/user-guides/rems/Handler-RequestReviewOptions.png" Alt="REMS Application Request Review Previews" Desc="REMS Application Request Review Previews" Title="REMS Application Request Review Previews" Ref="LDaCA" >}}

<br>

- A _Comment_ text field and an **_Upload_** button are available for either of the options **_from existing user_** or **_via email_**. Existing users are those listed in the “_Send requests to_ drop-down list. Select **_via email_** to send to an email address that is not listed.
  > It is important to document the details of the request – add them in the _Comment_ text field. The information provided will be saved and be available only from the application record. Comments are not sent via the standard email notifications.
- The Reviewer will need to log in to LDaCA REMS to view the comments and any uploaded material.

<br>

#### Request decision

- Use this option to obtain or follow up on a decision to approve or reject the application from whoever has the authority to decide.

{{< image Src="/user-guides/rems/Handler-RequestDecision.png" Alt="REMS Application Request Decision" Desc="REMS Application Request Decision" Title="REMS Application Request Decision" Ref="LDaCA" >}}

<br>

- This process is similar to the [Request Review](#request-review) option above.

<br>

#### Remark

- Select this option to add information in the _Comment_ text field. Tick the **_Show to applicant_** box if the information is meant to be visible to the Applicant.

{{< image Src="/user-guides/rems/Handler-Remark.png" Alt="REMS Application Remark" Desc="REMS Application Remark" Title="REMS Application Remark" Ref="LDaCA" >}}

<br>

- Click **_Remark_** when done.

<br>

#### Close application

- Select this option to close an application which will cancel the Applicant's access rights, e.g. at the end of the research period or the agreed expiry.

{{< image Src="/user-guides/rems/Handler-CloseApplication.png" Alt="REMS Close Application" Desc="REMS Close Application" Title="REMS Close Application" Ref="LDaCA" >}}

<br>

#### PDF

- This option is for producing a PDF document of the summary of an application. Information includes the Application number, name of the resource and license and the Events list.

<br>

#### Assign external id

- Handler can assign a user-friendly name for the application which is appended to the application ID which has the default format YYYY/##, e.g. “2024/28 - Smith Project” where “Smith Project” is the assigned external id.

<br>

## Revoke Entitlements

Follow the procedure in [Revoke entitlements](../owner-guide/#revoke-entitlements) of the Owner Guide.

<br>

## Manage the Deny List

Refer to [4.3 Managing the Deny List](../owner-guide/#43-managing-the-deny-list) of the Owner Guide.

> Do not delete any applications including drafts - it is important to keep a complete historical documentation of applications and decisions taken. This excludes drafts deleted by the Applicants themselves.

<br>
