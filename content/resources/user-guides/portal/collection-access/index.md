---
title: "Portal Collection Access"
date: 2018-01-29T11:38:46+11:00
draft: false
description: "A guide to viewing and applying for access to collections in the portal."
---

<br>

> This user guide uses 'portal' to refer to the interface across all of the available {{< glossary_link display="Oni" id="oni" >}} portals (see [Available Portals](/resources/user-guides/portal/available-portals/) for more details).

<br>

##### [Apply for Access to Collections with Access Restrictions](#apply-for-access-to-collections-with-access-restrictions)

##### [Apply for a Data License](#apply-for-a-data-license)

##### [View your Current Access List](#view-your-current-access-list)

<br>

## Apply for Access to Collections with Access Restrictions

When viewing an item that has restricted access, you will see one of the following permission warnings, depending on whether or not you are logged in to the portal:

- You do not have permission to see these files. Sign up or Login
- You do not have permission to see these files. You are logged in and you can apply for permission to view these files apply for access or refresh permissions

<br>

{{< image Src="/user-guides/portal/REMS-ApplyOrRefreshPermissions.png" Alt="Restricted Access Example" Desc="Restricted Access Example" Title="Restricted Access Example" Ref="LDaCA" >}}

<br>

Once you have logged in to the {{< glossary_link display="LDaCA" id="ldaca" >}} portal (see [Login](/resources/user-guides/portal/login/) for further details), select **_apply for access_** in the warning text and you will be directed to the LDaCA-{{< glossary_link display="REMS" id="rems" >}} login page in a new tab.

{{< glossary_link display="REMS" id="rems" >}} (Resource Entitlement Management System) is an open-source tool for managing access rights to resources such as research datasets. REMS is used by many research and government organisations. In this document, LDaCA-{{< glossary_link display="REMS" id="rems" >}} refers to the specific way REMS is implemented in the LDaCA environment.

<br>

{{< image Src="/user-guides/portal/REMS-WelcomeLogIn.png" Alt="LDaCA-REMS Interface Welcome Page" Desc="LDaCA-REMS Interface Welcome Page" Title="LDaCA-REMS Interface Welcome Page" Ref="LDaCA" >}}

<br>

Select **_Login_** and follow the CILogon prompts (see [Login](/resources/user-guides/portal/login/) again).

<br>

Once logged in, you will be presented with the license application form containing the following five sections:

- **State**: Shows the status of your application across three states:
  - **Apply**: Displays a tick mark when you click the **_Accept Terms_** button in the Licenses section.
  - **Approval**: Displays a tick mark when you click **_Submit application_** in the Actions section.
  - **Approved**: Displays a tick mark when your application is approved.
- **Applicants**: Shows the name of the Applicant and an **_Invite member_** button that allows the Applicant to send a link to the license application page to another person; the invitee will be prompted to log into LDaCA-{{< glossary_link display="REMS" id="rems" >}}.
- **Resources**: Provides a link to the license document.
- **Licenses**: Provides a link for the Applicant to view the license and an **_Accept license_** button to accept the terms.
- **Actions**: Contains features actionable by the Applicant, including **_Submit application_**, an important function to select during the application process.

<br>

{{< image Src="/user-guides/portal/REMS-Vanilla-SubmitApplication.png" Alt="LDaCA-REMS Interface Submit Application" Desc="LDaCA-REMS Interface Submit Application" Title="LDaCA-REMS Interface Submit Application" Ref="LDaCA" >}}

<br>

You will also notice the three top menu items, Catalogue, Applications and About:

- **Catalogue**: Lists resources to which you can apply for access.
- **Applications**: Lists all your applications, each with details such as the application ID, resource name, state and activity dates.
- **About**: A brief description of the LDaCA-{{< glossary_link display="REMS" id="rems" >}} tool.

<br>

## Apply for a Data License

{{< glossary_link display="Data licensing" id="data-license" >}} is the mechanism used in LDaCA-{{< glossary_link display="REMS" id="rems" >}} for {{< glossary_link display="data stewards" id="data-steward" >}} to grant or deny legal permission to access and use data.

The image below shows how to apply for a {{< glossary_link display="data license" id="data-license" >}} in three steps:

1. Go to _Licenses_ to read the license terms. Clicking on the link will open these in a new tab.
2. Then, still under _Licenses_, select **_Accept license_**.
3. Go to _Actions_ and select **_Submit application_** to activate the approval process.

<br>

{{< image Src="/user-guides/portal/REMS-SubmitApplication-Anon-123.png" Alt="LDaCA-REMS Application Submission Steps" Desc="LDaCA-REMS Application Submission Steps" Title="LDaCA-REMS Application Submission Steps" Ref="LDaCA" >}}

<br>

> Note that the application form above illustrates a basic license application procedure. Access restrictions and procedures for application approval will vary across {{< glossary_link display="collections" id="collection" >}} (e.g. requiring Applicants to complete a questionnaire, or to upload material explaining intended use of the data). {{< glossary_link display="Data stewards" id="data-steward" >}} can set up the license application approval as an automated process (using bots) which takes 1-2 minutes to complete. Other data stewards might prefer to receive, review and approve or reject the application themselves, or designate a colleague for the task. Understandably, human-mediated approval is likely to take longer than an automated process.

<br>

Every Applicant will be sent an email notification confirming the submission of a license application, and another email confirming approval.

Once approved, you should see all three tick marks under _State_:

<br>

{{< image Src="/user-guides/portal/REMS_LicenseApplication-Approved.png" Alt="LDaCA-REMS State: Application Approved" Desc="LDaCA-REMS State: Application Approved" Title="LDaCA-REMS State: Application Approved" Ref="LDaCA" >}}

<br>

Navigate back to the data {{< glossary_link display="object" id="object" >}} you require. If the warning text is still displayed, click **_refresh permissions_**. The page will update and you should be able to access the data. Note that these permissions apply to other data objects in the {{< glossary_link display="collection" id="collection" >}} that are covered by the same license terms; you do not need to apply for permission for each data object.

<br>

## View your Current Access List

To view your current list of licenses you have access to, hover your cursor over the arrow next to your account name to trigger a dropdown menu and select **_User Information_**. If you are not logged in, see the steps under [Login](/resources/user-guides/portal/login/). The _User Memberships_ section shows your current access list, and you can click **_Check Memberships_** to refresh this list. You can also select **_Verify your access in REMS_** to log into LDaCA-{{< glossary_link display="REMS" id="rems" >}}.

<br>

{{< image Src="/user-guides/portal/REMS-UserMemberships.png" Alt="LDaCA-REMS User Memberships" Desc="LDaCA-REMS User Memberships" Title="LDaCA-REMS User Memberships" Ref="LDaCA" >}}

<br>
