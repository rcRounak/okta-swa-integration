
# Integrating External Web Application Using Secure Web Authentication (SWA)

Here understand what is **Secure Web Authentication (SWA)** and we will also learn how to integrate an external web application like HackerRank with **Okta** using **Secure Web Authentication(SWA)** protocol.

## Prerequisite learning

OKTA IDaaS.

## What is Secure Web Authentication (SWA) ?
Secure Web Authentication is a technology which provides feature of **Single Sign on (SSO)** to the web applications which does not support protocols like **Security Assertion Markup Language(SAML)**, or **OpenID Connect(OIDC)**. Here we have flexibility that both user or administrator can set the credentials for the application. The credentials are stored in a safe, secured store which is **AES-256 encrypted**. When the credentials are set, the end user only needs to authenticate with **Okta** and they can Single Sign On directly into the application.  
If the administrators do not set the credential, **Okta** prompts the user to set the credentials for the first time. Now Okta will also prompt the user to install the **Okta Browser Plugin** into their web browser which will get the credentials and inject them directly into the external web application's sign in page and this way the user can sign in to the external web application.

## Integrating HackerRank with Okta
- If we already have access to **Okta** portal we can continue with the next steps.
    - Else we can get a [trail version](https://www.okta.com/free-trial/) or we can create a [developer account](https://developer.okta.com/). 
        
- We will sign in to our **Okta** portal.

- Go to **Applications** on the left side menu.

- Select **Create App Integration**.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/1.png)

- Next select **SWA - Secure Web Authentication** as **Sign-in method** and proceed with **Next**.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/2.png)

- Next we will go to the **HackerRank** website and create an account if we don't have one already.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/4.png)

- Lets go to the **login** page next and copy the link of the website.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/3.png)

- Now we can go back to the **Create SWA Integration** page in **Okta**.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/5.png)

- Give the application name as shown above.


- We need to give the **App's login page URL** which will be the login page url of the **HackerRank** which we just copied.


- Next we can also include the **App logo** if we want to add.

- Below this section we have second section where we need to specify **Who sets the credentials?**. Here we will select **User sets username and password** as we can see from the picture below.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/6.png)
- Next we will select the **Application username** as email because in the **HackerRank** login page we need to provide the email instead of the  username.
![](https://github.com/rcRounak/okta-swa-integration/blob/479871530ea2cec979cfeb0bd4637599356ce5a6/7.png)

- We will click on finish and proceed further.


- Next it is time to assign the application created to a user. So we will click on **Assign** button.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/8.png)
- Now we will select **Assign to People**.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/9.png)
- Select the user to whome we want to assign.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/10.png)
- Now we will go to the dashboard and click on our application to open it.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/11.png)
- We will see a **Sign In To App** where we need to provide our credentials which will be used in our **HackerRank** website to log in.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/12.png)
- Next click on **sign in**.

- We will also get a prompt to add **Okta Browser Plugin** to our web browser. Becuase this plugin will inject the credentials to the **HackerRank** website and we will be successfully logged in.

- Now if we want to access our application with the link instead of visiting our **Okta dashboard**. We will go to **General** tab under the application.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/13.png)
- And scroll down to the bottom where we will get the link under the **Embed Link** section. We can use this link.
![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/14.png)
- If we use this link, we will first need to get authenticated in the **Okta Signin Page** and only after successful authentication our connection will get redirected to the **HackerRank website** and we will be able to access the website without signing in further in the external web application (HackerRank here) as the credentials will get injected by the **Okta Browser Plugin**.

##  Verifying the connection

We will now verify the connection.

- We will open a browser and go to the **Okta Application Dashboard** and open our application.

![](https://github.com/rcRounak/okta-swa-integration/blob/aae36863862fd83fbd04fa67a60fffc328621df1/Secure%20Web%20Demo.gif)

- We can see our connection got redirected to the **HackerRank login page** and we can sign in to our **HackerRank** account without providing our username and password.

## Lessons Learned

How to integrate an **External Web Application (like HackerRank over here)** with **OKTA IdaaS** using **Secure Web Authentication(SWA)** protocol.

## Authors

- *[Rounak Roy Chowdhury](https://github.com/rcRounak)*

## Feedback

If you have any feedback, please reach out to me at rounakroyc23@gmail.com.


