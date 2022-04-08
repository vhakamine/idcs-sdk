Steps to configure social login

Create an application on Facebook

1. First step is to create an application in facebook to facilitate social login.
FacebookCreateApp

2. Once an application is created, select Social login product and configure it.
FacebookSelectProduct

3. Enable OAuth login flow and enter IDCS callback URL as OAuth redirect URL. The URL is https://IDCS_INSTANCE.identity.oraclecloud.com/oauth2/v1/social/callback
SocialLoginConfiguration

4. Copy client ID and client secret of the application. We will use that while configuring social login in IDCS.
ClientCreds

IDCS configuration
1. Login to IDCS with a user who has either Security administrator or Identity domain administrator privilege.
2. From the Settings tab, open Identity Providers configuration.
3. Click on Add Social IDP to add new social provider.
IDCSCreateSocialIDP

4. Enter Name and description of the provider and click Next button.
IDCSFacebookIDP

5. Enter client ID and client secret that you captured in the last step of creating an application in facebook.
FacebookIDPConfiguration

6. Activate the provider.
7. Now enable "Show on the login page" option to provide an option to login with Facebook credentials. Assuming that federation is activated for the instance, user will get an option to login with facebook credentials.
EnableFacebookProvider

Test social login
1. Once facebook social login is added and activated, try to login to an application or IDCS portal (https://IDCS_INSTANCE.identity.oraclecloud.com/ui/v1/myconsole).
2. On the login page, select facebook social provider to login with.
3. Once user is logged in through facebook, if user already has an account in IDCS, user will be logged in. If user does not have an account, then user gets an option to register and create an account in IDCS.
RegisterAccount

4. Enter additional details on the registration page and click on Register to button to finish registration process.
FinishUserRegistration

5. Once user account is created, user is sent activation email address and user gets an access to the application.
The process of adding any other supported social provider is same. You have to create an application on social login provider and capture client ID and secret. Add an additional provider from IDCS and enter respective client ID and secret.
