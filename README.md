# 🔐 SAML SSO Integration with Microsoft Entra ID 


## 🎯 Project Objective
This project demonstrates how to configure Single Sign-On (SSO) between Microsoft Entra ID and the Box cloud application using the SAML 2.0 protocol. The goal was to practice integrating a real SaaS application with Entra ID and simulate the authentication flow.

---

## 🛠️ Steps Taken

### 1. Added the Box Application
- Navigated to **Microsoft Entra ID > Enterprise Applications**
- Searched for **Box** in the application gallery
- Selected and created the Box app in my tenant

Box app overview page

<img width="1280" alt="Screen Shot 2025-05-09 at 6 08 33 PM" src="https://github.com/user-attachments/assets/aeb153e2-4bb9-456d-98a7-8ff695d156d6" />

---

### 2. Configured SAML-Based SSO
- Opened the **Single sign-on** settings for the Box app
- Chose **SAML** as the SSO method
- Entered the following values in the Basic SAML Configuration section:
  - **Identifier (Entity ID)**: `https://box.net`
  - **Reply URL (ACS URL)**: `https://sso.box.com/sp/ACS.saml2`
  - **Sign-on URL**: `https://account.box.com/login`
- Left Relay State and Logout URL blank
- Verified default attribute & claim mappings were pre-filled correctly

 Basic SAML Configuration + Attribute & Claim Mappings  

 <img width="1280" alt="Screen Shot 2025-05-09 at 6 23 21 PM" src="https://github.com/user-attachments/assets/01422504-c257-43b0-9352-00507dcecf3a" />


---

### 3. Assigned Users
- Went to the **Users and Groups** tab for the Box app
- Assigned two test users created in my Entra tenant

Assigned users screen

<img width="1280" alt="Screen Shot 2025-05-09 at 6 27 56 PM" src="https://github.com/user-attachments/assets/916e3942-53ca-461b-97e0-29b0bf790a25" />


---

### 4. Tested SSO Integration
- Used the built-in **Test Single Sign-On** feature in Entra
- Logged in with a test user
- Was redirected to Box, confirming the SAML assertion was successfully accepted

SSO test result showing redirection to Box

<img width="1280" alt="Screen Shot 2025-05-09 at 6 26 08 PM" src="https://github.com/user-attachments/assets/b51dc582-03a9-4aa1-a525-ba82e0d04b22" />


---

## 📈 What I Learned
- How to configure SAML SSO for a SaaS application
- Where to enter SAML URLs and manage claims in Microsoft Entra ID
- How to assign users and simulate real-world federated login flows
