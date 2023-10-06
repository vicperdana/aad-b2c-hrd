# Azure AD B2C: authenticate with the same email account against multiple identity providers
This project uses b2c custom policy to redirect users to different identity providers depending on domain_hint value.

# Scenario
In a multitenant system, it's common to have multiple identity providers (IdP) to authenticate users.  For example, you may have a system that allows users to log in using their social media accounts e.g., Facebook, Google, Twitter, etc.  You may also have a system that allows users to log in using their corporate accounts e.g., Azure AD, Okta, etc.  In this case, you may want to allow users to log in using the same email address but redirect them to different IdP depending on the domain name of the email address.  For example, if the user's email address is `joe@outlook.com`, you may want to redirect them to the social media IdP.  If the user's email address is `joe@companyxyz.com`, you may want to redirect them to the corporate IdP.  This is doable in Azure AD B2C using domain hint.  

Another possible scenario is to use the same email address to authenticate against multiple identity providers. You can pass on `trial1` and `trial2` as domain hints as part of query parameters. 

See below illustration for more info. 
