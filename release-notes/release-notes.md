# Delta Release Notes

## Delta 2.4

### Delta 2.4 - Release in progress

- Delta Document Storage 2.4.0:
  - Document AI insights:
    - AI-powered document classification and analysis (data extraction).
    - Supported AI providers: Microsoft Azure Document AI and Mistral.
    - Supported post-processing: Default, Invoice, CNS, MRZ.
  - Ability to consult dispatcher traces related to Delta Document Storage.
- Delta Customer Portal 2.4.0:
  - Developer technical documentation improvements:
    - Access to the definition history of Delta APIs.
    - Comparing versions of Delta APIs.
    - Delta custom formats documentation.
  - Ability to disable developer pages.
- Delta Process 2.4.0:
  - Delta VS Add-in: support for VS2019 dropped, VS2022 is now required.
- Delta Ldap worker service 2.4.0:
  - Strengthen user access rights.
- Ability to disable Swagger UIs for all Delta APIs.
- Ability to request authentication with additional custom claims.
- Functional release notes available on GitHub and from the Customer Portal (About page).
- Minor bug fixes and improvements.

## Delta 2.3

### Delta 2.3 - Patch 16/10/2025

- Delta Document Storage 2.3.1:
  - Option to soft-delete, hard-delete and retrieve soft-deleted documents.
  - Characters '[' and ']' supported for meta tag names, model names, document names and headersheet reference.
  - OCR requests processed in an interleaved manner across tenants, improving efficiency and reducing wait times.
- Delta Legal Archiving 2.3.1:
  - Improved compatibility with Arcsys 2024.2.0 LTS.
- Delta Monitoring 2.3.1:
  - Email alert when an API availability status changes.
- Security:
  - Ability to configure traffic rate limiting per user.
  - HTTP security headers added.
  - JS scripts minification and obfuscation.
  - Ability to configure user cookie maximum expiration dates.
  - Ability to use virus scanning (ClamAV) on file upload.
  - Ability to validate file extension and mime on file upload.
- Bug fixes:
  - [#3011] Delta portals: the loading indicator stays visible on the list pages when the user goes back to the previous page. 
  - [#3082] Delta E-signature Portal: Remote Server Error when interacting with Nowina API.
  - [#3090] Delta Document Storage Portal: tree view filter not working as expected with empty meta tag value.
  - [#3121] Delta E-signature: Remote Server Error while interacting with LuxTrust API.
  - [#3123] Delta Emailing: some emails are rejected (considered invalid) by Delta.
  - [#3052] Delta Emailing: IMAP protocol not working with Office365.
  - [#3157] Delta Document Storage: document trace permission (CanReadActivityLog) not applied.
  - [#3158] Delta Integration Tests: some integration tests no longer works with Chrome v138.0.7204.101.
  - [#3195] Delta E-signature: inconsistent Luxtrust error message.
  - [#3198] Delta Document Storage: invalid file name extension on OCR request.
  - [#3199] Delta Document Storage Portal: inconsistent error message when submitting a new document request with non-PDF files.
  - [#3200] Delta Document Storage Portal: special characters of file name changed to underscore on file download.
  - [#3201] Delta Document Storage: obsolete image file formats (pjpeg, x-png) not supported.
 
### Delta 2.3 - Release 10/03/2025

- Delta Document Storage 2.3.0:
  - Document soft deletion.
  - Accented characters supported for meta tag names, model names, document names and headersheet reference.
- Delta Process 2.3.0:
  - Performance improvement of SQL read queries.
  - Accented characters supported for meta tag names.
  - Workflow meta tag management (single/multiple values).
  - Meta tag filter expression improvement (multiple value management on right operand of comparison operations).
  - Workflow cache management API for administrators.
- Delta E-signature 2.3.0:
  - Nowina audit trail management.
- Delta Email 2.3.0:
  - IMAP OAuth authentication option.
  - SMTP OAuth authentication option.
- Delta Customer Portal 2.3.0:
  - Workflow instance filter improvements.
  - Workflow instance traces grouped by execution run.
  - Workflow meta tags management.
- Isolation of PDF manipulations in a new open source project (Sitl.PdfHelper) that conforms with iText AGPL license.
- SSL option for all Delta Windows services.
- App settings auto reload at runtime.
- Migration .Net6.0 to .Net8.0.
- Migration UI controllers to Razor Pages.
- Licence notice.
- Minor bug fixes and improvements.

## Delta 2.2

### Delta 2.2 - Patch 14/02/2025

- Bug fixes:
  - [#2856] Delta Process: performance degradation issue.
  - [#2857] Delta Document Storage: issue with large request bodies when uploading big documents.
  - [#2879] Delta Insurance: CAA sync no longer works (CAA web site changed on feb 2025).

### Delta 2.2 - Patch 6/01/2025

- Bug fixes:
  - [#2806] Delta Email: email (Brevo) resend issue.
  - [#2809] Delta Process: performance issue.
  - [#2831] Delta Customer Portal: filter is not applied when selecting 'Show more' on the workflow instance list page.
  - [#2832] Delta Document Storage: meta tag names containing the character '&' cause an error when a filter is applied.

### Delta 2.2 - Patch 4/12/2024

- Bug fixes:
  - [#2746] Delta Email: Brevo webhook not filtered by environment.
  - [#2789] Delta Document Storage and Delta Process: performance degradation when user role security is enabled.
  - [#2792] Delta Email: performance optimization.
  - [#2797] Delta Master: performance optimization.

### Delta 2.2 - Patch 18/11/2024

- Bug fixes:
  - [#2733] Delta Document Storage and Delta Process: error on database creation/migration (SQL 'SetContext' does not exist).
  - [#2737] Delta Process: error on WF workflow instance deserilization (wrong assembly name).

### Delta 2.2 - Patch 11/11/2024

- Delta Process 2.2.3:
  - Ability to limit engine request concurrency.
  - Ability to preload workflows on start.
  - Performance improvements:
    - Isolation of WF process engine in separate service to optimize performance.
    - Workflow loading concurrency lock improvement.
    - SQL connection recycling improvement.
    - Various SQL optimizations.

### Delta 2.2 - Patch 2/11/2024

- Bug fixes:
  - [#2721] Performance degradation due to app settings loading.

### Delta 2.2 - Patch 22/10/2024

- Logging warning slow SQL queries.
- Bug fixes:
  - [#2685] Delta Process Add-in: user security roles showing twice when a user role has been deleted.
  - [#2699] Delta Process: usage trace generated despite being disabled.
  - [#2703] Delta Process: empty in-argument misinterpreted.

### Delta 2.2 - Patch 11/10/2024

- Delta Process 2.2.2:
  - New in-argument 'EnableTryMode' on activities 'ResumeWorkflowInstance' and 'StartNewWorkflowInstance'.

### Delta 2.2 - Patch 10/10/2024

- Delta Process:
  - Workflow loading performance optimization.
  - Workflow trace storage deferral option.
  - Improved readability of workflow traces.
- Bug fixes:
  - [#2680] SQL connection timeout misconfigured.

### Delta 2.2 - Patch 4/10/2024

- Delta Document Storage 2.2.2:
  - Additional characters (<>=~()[]) supported for meta tag string values.
- Technical documentation update.

### Delta 2.2 - Patch 27/09/2024

- Delta Document Storage 2.2.1:
  - Exclude delivery item option from future AGI jobs.
  - Delivery job label included in Brevo tags.
- Bug fixes:
  - [#2573] Delta Document Storage Portal: error on step1 of the document add bundle wizard page: 'The view component matched multiple types'.

### Delta 2.2 - Patch 5/08/2024

- Delta Monitoring: 
  - New API to retrieve the latest uptime log state.
- Bug fixes:
  - [#2588] Delta Document Storage: invalid Tesseract service URL.
  - [#2589] Delta Document Storage: invalid Tesseract configuration parameters.

### Delta 2.2 - Patch 10/07/2024

- Migration Pdfjs 4.4.168.
- Bug fixes:
  - [#2585] Delta IntegrationTests: Selenium chrome driver not properly disposed.
  - [!787] Delta Document Storage: invalid Brevo notification order.

### Delta 2.2 - Patch 3/07/2024

- Delta Process 2.2.1:
  - Bug fix #2575.
- Delta Insurance:
  - IVASS sync no longer works (IVASS web site changed on june 2024).
- Delta Document Storage:
  - Isolation of Tesseract OCR in separated service to optimize performance.
- Bug fixes:
  - [#2576] Delta Process (proxy): unencoded URLs causing 404 errors.

### Delta 2.2 - Release 26/05/2024

- Delta Master 2.2.0:
  - Subscription key email management.
  - New user permission for Delta portals access.
- Delta E-signature 2.2.0:
  - Migration to Nowina EVA Portal v3.10.
- Delta E-signature Portal 2.2.0:
  - Access portal features through API.
  - Option for signatories to define the signature location through Eva portal.
  - Enable/disable signature bulk mode.
  - ADFS-based login mode.
- Delta Process 2.2.0:
  - Dynamic update for running instances:
    - Ugrade the workflow version (WF only).
    - Modify variable value.
    - Adjust expiration time of the Delay activities.
- Delta Email 2.2.0:
  - Support for sending email through Brevo API.
- Delta Document Storage 2.2.0:
  - Email delivery via Brevo or via classic SMTP.
- Delta Document Production 2.2.0:
  - Instruction counting on document merge.
  - Document merging in drive mode through the Delta Word Add-in.
- Portal cookie path improvements.
- Build metadata storage at project level.
- Chrome driver auto-update before integration tests.
- Minor bug fixes and improvements.

## Delta 2.1

### Delta 2.1 - Patch 14/02/2025

- Bug fixes:
  - [#2832] Delta Document Storage: meta tag names containing the character '&' cause an error when a filter is applied.
  - [#2857] Delta Document Storage: issue with large request bodies when uploading big documents.

### Delta 2.1 - Patch 2/10/2024

- Bug fixes:
  - [#2658] Delta Dispatcher (worker service): logging causing unhandled errors.

### Delta 2.1 - Patch 5/08/2024

- Delta Monitoring: 
  - New API to retrieve the latest uptime log state.
- Bug fixes:
  - [#2588] Delta Document Storage: invalid Tesseract service URL.
  - [#2589] Delta Document Storage: invalid Tesseract configuration parameters.

### Delta 2.1 - Patch 10/07/2024

- Migration Pdfjs 4.4.168.
- Bug fixes:
  - [#2585] Delta Integration Tests: Selenium chrome driver not properly disposed.

### Delta 2.1 - Patch 3/07/2024

- Delta Document Storage:
  - Isolation of Tesseract OCR in separated service to optimize performance.

### Delta 2.1 - Patch 1/07/2024

- Delta Insurance:
  - IVASS sync no longer works (IVASS web site changed on june 2024).

### Delta 2.1 - Patch 17/06/2024

- Bug fixes:
  - [#2576] Delta Process (proxy): unencoded URLs cause 404 errors.

### Delta 2.1 - Patch 21/03/2024

- Bug fixes:
  - [#655] Delta Document Storage: opening email documents causes 403 errors.


### Delta 2.1 - Patch 23/02/2024

- Delta E-signature Portal 2.1.1:
  - New public API for interacting with the e-signature process.
- Delta Insurance:
  - FSMA sync no longer works (FSMA web site changed on feb 2024).
- Minor bug fixes and improvements.

### Delta 2.1 - Patch 1/02/2024

- Delta Process 2.1.1:
  - Ability to specify the role of a guest token.
  - Ability to reserve a code for a future workflow instance.
- Delta Pdf Viewer 2.1.1:
  - PDF page selector viewer.
- Minor bug fixes and improvements.

### Delta 2.1 - Patch 13/01/2024

- Minor bug fixes and improvements.

### Delta 2.1 - Release 30/11/2023

- Delta Document Storage 2.1.0:
  - Contextual pages (parts) available for embedding in external applications:
    - Document list page.
    - Document page.
    - New document wizard.
  - Ability to overwrite the last document version.
  - Tag filter expression improvement:
    - Multiple value management on right operand of comparison operations.
    - Performance optimizations.
  - Limiting supported character set for meta tag names, model names, document names and headersheet reference.
- Delta Process 2.1.0
  - New activity 'GetDocumentDeliveries'.
  - Limiting supported character set for meta tag names.
- Delta Email 2.1.0
  - New email send mode 'On hold'.
- Delta Insurance 2.1.0
  - Chrome driver auto update before IVASS sync process.
- Delta Monitoring 2.1.0:
  - Delta component uptime monitoring, including regular ping checks and statistics management.
- New authentication claims: email claim and elevated privileges permission claim.
- ADFS auto-challenge settings improved.
- Minor bug fixes and improvements.

## Delta 2.0

### Delta 2.0 - Patch 14/08/2023

- Bug fixes:
  - [!485] Delta Document Storage: job delivery causes unhandled exception.

### Delta 2.0 - Release 18/07/2023

- Delta Process 2.0.0:
  - Process engine available in 2 runtimes:
    - Microsoft WF (.Net48).
    - UiPath CoreWF (.Net6.0).
- Migration .NetCore3.1 to .Net6.0.
- Yaml release pipelines.
- Minor bug fixes and improvements.

## Delta Older Versions

Release notes for Delta versions earlier than 2.0 are no longer available. Please contact us for more information.
