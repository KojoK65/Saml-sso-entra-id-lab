# Saml-sso-entra-id-lab
# 📦 Box SSO Integration with Microsoft Entra ID (Azure AD)

## 🎯 Project Objective
This project demonstrates how to configure Single Sign-On (SSO) between Microsoft Entra ID and the Box cloud application using the SAML 2.0 protocol. The goal was to practice integrating a real SaaS application with Entra ID and simulate the authentication flow.

---

## 🛠️ Steps Taken

### 1. Added the Box Application
- Navigated to **Microsoft Entra ID > Enterprise Applications**
- Searched for **Box** in the application gallery
- Selected and created the Box app in my tenant

📸 *Screenshot: Box app overview page (Enterprise Apps > Box)*  
![Box App Overview](screenshots/box-app-overview.png)

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

📸 *Screenshot: Basic SAML Configuration + Attribute & Claim Mappings (captured together)*  
![SAML Config and Claims](screenshots/saml-config-and-claims.png)

---

### 3. Assigned Users
- Went to the **Users and Groups** tab for the Box app
- Assigned two test users created in my Entra tenant

📸 *Screenshot: Assigned users screen*  
![User Assignment](screenshots/user-assignment.png)

---

### 4. Tested SSO Integration
- Used the built-in **Test Single Sign-On** feature in Entra
- Logged in with a test user
- Was redirected to Box, confirming the SAML assertion was successfully accepted

📸 *Screenshot: SSO test result showing redirection to Box*  
![SSO Test Result](screenshots/sso-test-result.png)

---

## 📈 What I Learned
- How to integrate a real SaaS application using SAML SSO
- Where and how to configure SAML URLs in Microsoft Entra
- How user identity data (claims) is passed during authentication
- How to assign users to an enterprise app and test the full sign-on process
