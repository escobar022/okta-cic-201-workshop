+++
title = "Prerequisites"
chapter = false
weight = 20
pre = "<b>1. </b>"
+++
To follow this workshop, you’ll need access to Okta Demo Platform.

### 1. Create a Demo Platform account
You need access to the Okta Demo Platform. We provide an Okta CIC (Auth0) Tenant via demo.okta.com.

#### Demo Platform Partner Sign Up (preferred option)
This method is preferred because your access to demo.okta.com will not automatically expire.

1. [Click here to access the demo platform](https://demo.okta.com/).
2. If you are a partner, use the **Continue with Okta Partner**. 
3. This will route you to partner.okta.com where you will log in with your partner credentials.
4. If you do not yet have credentials for partner.okta.com, please click the link “Request Okta Partner Community Access” and submit your application. **It may take a few business days for your application to get approved.**

#### Demo Platform Sign Up as Guest (backup option)
This method is considered "backup" because you will only be able to sign-in with this guest access for 24 hours.

1. [Click here to access the demo platform](https://demo.okta.com/).
2. If you are a guest or don't have a partner account yet, use the **Continue with Okta Guests**.

### 2. Generate an Okta CIC (Auth0) demo tenant

1. Once authenticated into demo.okta.com, click on the tile labeled "Demo Builder"
2. A new tab will open. Click on "+ New Demo"
3. Under Purpose, select the radio button for "Personal Enablement / Accreditation"
4. Under Identity Platform, select the radio button for "Customer Identity Cloud"
5. Under Name, give your tenant a name (this is a global namespace, so I recommend using a naming format like **myname-cic-workshop**)
6. Click "Create"
7. Your CIC tenant is now spinning up. It will take 5-10 seconds to generate. Wait for the green check mark and "Active" to show up before you can proceed.
8. Once Active, click "Accept Invitation" (this is a one-time task to enter your CIC tenant the first time)
9. Click through all "continue" redirects
10. You are now in your CIC tenant admin console!