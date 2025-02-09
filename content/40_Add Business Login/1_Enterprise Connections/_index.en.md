+++
title = "Enterprise Connections"
chapter = false
weight = 10
pre = "<b>4.1 </b>"
+++

Enterprise Connections in Auth0 allows external users to authenticate with Identity Providers (IdP) such as Okta, Google Workspace, and more.

We will configure Okta as an Enterprise Connection. 
<!-- You have 2 options in this workshop to get the configuration parameters: -->

<!-- 1. Create a new Okta Tenant and do the integration by yourself (free, no credit card required)
2. Use the Workshop Org Creator (might not work) -->

<!-- ### 1. Create a new Okta Tenant and do the integration by yourself  (free, no credit card required)

The first step is to create a new Okta Tenant. If you have already one, you can also use it.

1. [Click here to create your free Okta account.](https://developer.okta.com/signup) No credit card is required.
2. Select **Sign up free for Developer Edition**.
3. You will receive an Email. Click on the link to activate your account.
4. Set the password of your Okta Account and you are ready to go.

Login to the **Okta Admin Console**. If you see the Okta Dashboard, click on the **Admin** button in the top right corner.
![Okta - Dashboard login to Admin](../images/40_10_okta_dashboard_admin.png)

1. In the navigation bar on the right of the Okta Admin Console, go to **Applications** -> **Applications** and click on **Create App Integration**.
![Okta - Create OIDC Application](../images/40_20_okta_create_oidc.png)
3. Select **OIDC - OpenID Connect** and **Web Application** click on **Next**.
![Okta - Select OIDC Application Type](../images/40_30_okta_select_oidc_app_type.png)
4. Provide the following information
    - **App integration name**: `Auth0 Org1`
    - **Sign-in redirect URIs**: `https://{Auth0-Tenant-ID}.{us/eu}.auth0.com/login/callback`
        - You can find the name by going to https://manage.auth0.com/dashboard/region/tenant-name
        - As an alternative, to get it working in this Workshop, select **Allow wildcard * in login URI redirect** and use `https://*.{us/eu}.auth0.com/login/callback`
    - Select **Allow everyone in your organization to access**.
    - Click on **Save**.
![Okta - Create OIDC Application](../images/40_40_okta_create_oidc.png)
5. Copy the following values:
    - **ClientID**
    - **Client Secret**: Scroll down to the section **CLIENT SECRETS** and click on the Copy button next to the generated secret.
    - **Okta Domain**: This is the domain of your Okta Tenant. Copy it from the URL of the browser and remove **-admin** e.g. `my-domain.okta.com` -->

### 1. Workshop Org Creator

<!-- As an alternative to Step 1, we are providing sample organizations running on the Okta service. In order to create your organization, visit https://okta-cic-workshop-org-creator.herokuapp.com/. Here you will need to provide some information: -->
We have created a sample Okta Workforce tenant to simulate a business customer's employee single sign-on (SSO) implementation.
In a new tab, navigate to https://okta-cic-workshop-org-creator.herokuapp.com/

- **Auth0 Tenant Name**: This is the name of your own Auth0 tenant you are using at the moment, it is **not** the URL in your web browser. To find this value, go to your CIC tenant, click on Applications > Applications, click on Storytime, go to the Settings tab, and copy the value under "Domain" (the value will have the naming convention {tenant-name}.cic-demo-platform.auth0app.com). Be sure to copy the entire value under "Domain".
- **A name for your organization**: Use the naming scheme your-name-workshop or similar unique names to avoid conflict with other lab participants
- **Email address**: You can use any email address, though we recommend using an @example.com email, e.g. your-name@example.com.
- **First and last name are optional** and can be entered if you want to see that this information will be transferred to Auth0 later on as well

Once you have entered your details, you should receive a password for your user as well as a client ID that you can use to set up the SSO connection. Please note both as we will need it throughout the lab to login into Okta. **Do not close out of this tab!! You will need to reference the information throughout the rest of the lab**

### 2. Create Enterprise Connection
The final step is to register Okta as a new enterprise connection in Auth0.

1. In the navigation bar on the right of the **Auth0 Dashboard**, go to **Authentication** --> **Enterprise**.
<!-- 2. Click on the **+** of **Okta Workforce**. -->
2. Click on the **+** of **OpenID Connect**
3. Enter the following:
    - **Connection Name**: `Okta1`
    <!-- - **Okta Domain**: The value you copied earlier e.g. my-domain.okta.com -->
    - **Issuer URL**: The Issuer URL from the Org Creator (starts with "https://tu-playground.okta.com...")
    - **Client ID**: The value you copied earlier from the Org Creator output.
    <!-- - **Client Secret**: The value you copied earlier. -->
    <!-- - The required **Callback URL** that you configured in Okta is also displayed. If the login is not working, use it to validate that you configured the right value in Okta. -->
    - Scroll down and Click on **Create**.
<!-- ![Okta + Auth0: Configure Enterprise Connection](../images/40_50_okta_auth0_enterprise_configuration.png) -->
4. The tab **Login Experience** is shown.
5. Go to the section **Connection Button** and select **Display connection as a button**.
6. Click on **Save**.
7. Switch to the tab **Applications**.
8. Enable for **Storytime**.

### 3. Test
1. Navigate to your Storytime application and re-try the login. 
2. The button **Continue with {domain}.okta.com** shows up - click on it to sign-in.
3. You should be redirected to your newly created Enterprise Connection and be able to sign in with the credentials that you used to create your Okta Tenant or received when registering the organization.
4. Back at our Sample Application, you can get more details about the signed-in users in the top right corner.