+++
title = "Integrate Storytime Application"
chapter = false
weight = 30
pre = "<b>2. </b>"
+++
The sample application that we use in this Workshop is **Storytime**, a simple SPA built by the Okta Demo Engineering team. You are requested to evaluate Auth0 to provide the login and user management. In order to get started, make sure you have an Auth0 Tenant via the Demo Platform as shown in the previous chapter **Prerequisites**.

### 1. Add StoryTime Application via demo.okta
1. Back in in the Demo Platform, navigate to your recently spun up Demo (from the Prerequisites chapter)
2. Click on "+Add Application"
![Copy Domain and ClientID](images/AddStoryTimeApplication.png)
3. Find the Managed application named "Storytime" and click "Attach"
4. It will take a few seconds for the application to deploy (you'll see an hour glass and text "Deploying" in gray). Once deployed, the status will show a green check mark and "Active"
5. Click "Launch" to open the Storytime experience in a new tab
![Copy Domain and ClientID](images/Storytime_firstpage.png)

<!-- ### 1. Login to Auth0 Management Console
- If you're using a free trial tenant, sign in to https://manage.auth0.com
- If you're using a CIC tenant from demo.okta, open the management console of your tenant via https://demo.okta

### 2. Create a new Application
1. Go to **Applications** -> **Applications** and click on **+ Create Application**.
2. Enter as Name `CIC Workshop`, select **Single Page Web Application** and click on **Create**.
3. On the prompted Quick Start menu, choose **JavaScript**.
    - Auth0 provides instructions on how to integrate with your existing App or download an example application. We use the sample application cloned from the previous step.
4. Switch to the tab **Settings** and enter as **Allowed Callback URLs**, **Allowed Logout URLs** and **Allowed Web Origins** the callback URL of your application `http://localhost:3000` (If you use Cloud9, the URL is different).
5. Click on **Save Changes**.

![Copy Domain and ClientID](images/20_10_callback_url.png)

### 3. Integrate Application

1. Open the file **auth_config.json**, which is in the root folder of the cloned sample application.
2. Paste the **Domain** and **Client ID** from the **Settings**.
3. **Save** the file.

![Copy Domain and ClientID](images/20_20_Copy_Domain_ClientID.png)

### 3. Test
1. Save your project.
2. Start the application by typing `npm run dev ` into your terminal.
3. Navigate to `http://localhost:3000` and click on login in the top right corner.
    - If an error the error "This site can’t be reached", did you save auth_configuration.json?
4. Click on **Sign up** to create a new user.
5. Accept the consent screen and you are successfully signed in.
6. Click in the top right corner on **Profile** to see the ID Token that the application gets from Auth0.

![Copy Domain and ClientID](images/20_30_user_profile_page.png)

### 4. Next Step
- Congratulations, you now have a working login form!
- If you are doing this lab in a guided class, please wait for your instructor to continue the course.
- Otherwise, you may proceed to customize the user journey. -->