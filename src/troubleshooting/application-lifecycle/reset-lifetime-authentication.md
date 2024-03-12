---
summary: The article provides a solution for regaining access to LifeTime and Service Center after being locked out due to external authentication issues
locale: en-us
guid: ee89babf-f053-4269-8485-d75ff21a2a27
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---
# Reset LifeTime authentication preferences

This articles applies to self managed infrastructures.

## Symptoms

After changing the authentication to an external provider (for example, [Active Directory](https://www.outsystems.com/tk/redirect?g=f8b008aa-ae75-470a-adc3-5863bf6be8e6) or an [external IdP via OpenId Connect](https://www.outsystems.com/tk/redirect?g=595C5E6F-7C59-4314-9BDE-4EF1400A670F). You've been locked out of LifeTime, Service Center, and Service Studio and can't login.

## Cause

Usually this happens when there are incorrect configurations, thus failing all logins.

## Resolution

To resolve this issue, please run the following script in the databases of the LifeTime environment and all the environments that are registered in it:

`UPDATE OSSYS_AUTHPROVIDER SET ISACTIVE = 0;`

`commit;`

After that you will be able to login on LifeTime/Service Center with your previous credentials.

