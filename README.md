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

<img src="https://github.com/user-attachments/assets/16579ea8-3b92-4dae-b49b-8c1b89bcc4a3" alt="Enable SAML in Salesforce" width="450" />

2. I configured the SAML Single Sign-On settings in Salesforce by selecting **New from Metadata File**, clicking **Choose File** to upload the Federation Metadata XML file I had previously downloaded from my Microsoft Entra page, and then selected **Create**:

<img src="https://github.com/user-attachments/assets/5bb3da30-fb70-4fde-8557-9962df94b49e" alt="Upload Metadata to Salesforce" width="500" />

3. After uploading the file and clicking **Create**, Salesforce automatically generated metadata page with the metadata fields pre-filled with my Microsoft Entra information. I named this SAML configuration **EntraSSO** and clicked **Save**:

<img src="https://github.com/user-attachments/assets/b4ad167b-cec8-4bf5-8fac-742a3295e92c" alt="SAML Settings Generated" width="500" />

4. To enable the **EntraSSO** authentication method, I navigated to **Company Settings** > **My Domain** > **Authentication Configuration**, clicked **Edit**, selected the **EntraSSO** checkbox, and then clicked **Save**:

<img src="https://github.com/user-attachments/assets/d7c9c7e1-48c5-4b14-9633-9e3c1453cd76" alt="Enable EntraSSO in Salesforce" width="400" />

### Test SSO on a User

1. To test whether SSO was functioning correctly, I assigned the Microsoft Entra user **Pipa** to the Salesforce application. Then, I created a corresponding user account for **Pipa** on my Salesforce Developer site:
<p>
  <img src="https://github.com/user-attachments/assets/bdea96f4-19ad-46d0-973d-ef99590d85aa" alt="Assign Pipa in Entra" width="450" />
  <img src="https://github.com/user-attachments/assets/1d622aaa-f294-4280-9a58-5c28510a04de" alt="Create Pipa in Salesforce" width="450" />
</p>

2. After creating user **Pipa** account in Salesforce, I logged into the Microsoft My Apps portal using the same Pipa Entra account. The Salesforce application appeared on the dashboard. Upon clicking it, I was redirected to the Salesforce site without needing to sign in again, confirming that the SSO configuration was working successfully:

<p>
  <img src="https://github.com/user-attachments/assets/f519d564-e628-463a-a998-4fd6a888a9ee" alt="Salesforce on Entra Dashboard" width="450" />
  <img src="https://github.com/user-attachments/assets/2161395e-34a5-47eb-828a-9ec4ad98528f" alt="Logged into Salesforce via SSO" width="450" />
</p>

-------

## Conclusion

This project successfully demonstrates how to integrate Microsoft Entra ID with Salesforce using SAML-based Single Sign-On (SSO). By configuring both platforms and exchanging metadata, I enabled seamless authentication for users. The final test—logging in as the assigned Entra user and accessing Salesforce without re-entering credentials, validated that the SSO setup was functioning as intended. This integration enhances security and user experience by centralizing identity management through Microsoft Entra ID.









