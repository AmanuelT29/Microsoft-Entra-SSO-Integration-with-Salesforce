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
  <img src="https://github.com/user-attachments/assets/7d8f7c1b-1394-44c6-a4a7-7645cf3481ec" alt="Salesforce App Search" width="40%" />
  <img src="https://github.com/user-attachments/assets/30141af0-63a6-435d-ace1-ba0a4623178b" alt="Salesforce App Selection" width="35%" />
</p>


### Configure Microsoft Entra SSO

1. To configure Micrsoft Entra SSO for Salesforce, I navigated to **Enterprise applications** > **Salesforce** > **Single sign-on**. On the Select a single sign-on method page, I chose **SAML**. Then, on the **Set up single sign-on with SAML** page, I clicked the edit icon under **Basic SAML Configuration** to modify the required settings:

<img src="https://github.com/user-attachments/assets/9b10c18f-33b4-4885-af6f-2dd20099ad32" alt="SAML Configuration in Entra" width="400" />


2. On the **Basic SAML Configuration** page, I entered the required information from my Salesforce Developer account to complete the integration setup:

<img src="https://github.com/user-attachments/assets/18d81cc6-2c79-4181-a58f-8dd9008a2e74" alt="Basic SAML Configuration" width="400" />


3. On the **Set up single sign-on with SAML** page, under the SAML Signing Certificate section, I selected and downloaded the **Federation Metadata XML** file. I saved it on my computer to use later when configuring the SSO settings in my Salesforce Developer account:

<img src="https://github.com/user-attachments/assets/e1316e61-65d2-40dd-ae7f-c2bdc5423c2c" alt="Download Federation Metadata XML" width="400" />

### Configure Salesforce SSO

1. In my Salesforce Developer account, I ensured that the SAML feature was enabled by navigating to: **Setup** > **Identity** > **Single Sign-On Settings**, clicking **Edit**, selecting **Enable SAML**, and then clicking **Save**:

<img src="https://github.com/user-attachments/assets/16579ea8-3b92-4dae-b49b-8c1b89bcc4a3" alt="Enable SAML in Salesforce" width="400" />









