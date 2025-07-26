<p align="center">
  <img src="https://github.com/user-attachments/assets/bd4c09fd-cab4-4834-a7af-3e10c62309f3" alt="Screenshot 2025-07-03 211806" width="200" /><img src="https://cdn.worldvectorlogo.com/logos/salesforce-2.svg" alt="Salesforce Logo" width="150"/>


# Microsoft Entra ID SSO Integration with Salesforce

## Platform and Tools Used
- Microsoft Entra ID
- Salesforce
- Web Browser

## Objective
In this project, I demonstrate how to integrate Microsoft Entra ID Single Sign-On (SSO) with the Salesforce application. The process begins by adding Salesforce from the **Enterprise applications** section in Microsoft Entra. I then configure the SAML-based SSO settings in both Microsoft Entra and the Salesforce platform. Once both sides are properly configured, I test the integration by assigning a user in Microsoft Entra to access Salesforce using the SSO method.

---------

### Add Salesforce app in Microsoft Entra
To add the Salesforce application in Microsoft Entra, I navigated to **Enterprise applications** > **New application** (pic1), searched for **Salesforce** in the search bar, selected it from the results, and clicked Create (pic2) to add it to the tenant:
<p float="left">
  <img src="https://github.com/user-attachments/assets/7d8f7c1b-1394-44c6-a4a7-7645cf3481ec" alt="Salesforce App Search" width="49%" />
  <img src="https://github.com/user-attachments/assets/30141af0-63a6-435d-ace1-ba0a4623178b" alt="Salesforce App Selection" width="40%" />
</p>


