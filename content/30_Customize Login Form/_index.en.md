+++
title = "Customize Login Form"
chapter = false
weight = 40
pre = "<b>3. </b>"
+++
Our simple login is in place and users can sign in to our application. It looks very generic and lacks official branding. Customers can also not use Social Login which simplifies the sign-up rate.

### 1. Add Branding
1. In the navigation bar on the right of the Auth0 Dashboard, go to **Branding** -> **Universal Login**.
<!-- 2. Enter the logo as well as the primary and background color specified.
    - Logo: `https://pizza0lab.s3.eu-central-1.amazonaws.com/pizza.jpeg`
    - Primary color: `#EB5424`
    - Background color: `#3A3A3A`
3. Click on **Save**
4. Navigate to your application and retry the login (`http://localhost:3000`). -->
2. You'll notice that Storytime already has a customized Universal Login view. Click on **Customization Options** to enter the WYSIWIG editor.
3. From here, feel free to experiment with some different styling, such as Page Background > Page Layout left or right orientation.
4. Once you've made any changes, click "Save and Publish" in the top right. Upon refreshing Storytime, you'll see the updated Universal Login experience.

### 2. Add Social Login
1. In the Auth0 Dashboard, go to **Authentication** -> **Social** and click on **+ Create Connection**. (Google should be already listed as a provider.)
2. Select a provided where you have an account to test it afterward e.g. LinkedIn, Facebook ....
3. You don't have to follow the provided instructions, most applications come with Developer Keys that are fine for the Workshop to try them out. In production deployments, we would always recommend setting your own client ID and client secret.
4. After creating the Social Connection, the **Application** section is automatically shown. Enable it for the previously created **CIC Workshop** application.
5. Navigate to your application and retry the login, you will be able to use your social provider to access the application (`http://localhost:3000`).

### 3. Next Step
- Congratulations, you just made your application a lot more appealing!
- If you are doing this lab in a guided class, please wait for your instructor to continue the course.
- Otherwise, you may proceed to the next lab to make your platform fit for business customers and give them a great login experience!