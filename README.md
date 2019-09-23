# stock_module
A magento module extending uDropship that receives stock updates by email

# Requirements
Run composer install
Run modman
Need Google Oauth API
Need Google service account credentails

# Setup to connect with gmail api

## Requirements

1. gmail account - To create new gmail access api connection.
2. Client-id & client-secret - To access created app from php code.

## Get your google app credentials

```
Follow the 7 steps below
```
1. Open the ​Google API Console Credentials page​.
![Credentails](/readme/Page-1-Image-1.png)
2. Click ​ **Select a project​** , then ​ **NEW PROJECT​** , and enter a name for the project, and
    optionally, edit the provided project ID. Click​ **Create​**.
3. On the Credentials page, select ​ **Create credentials​** , then ​ **OAuth client ID​**.
4. You may be prompted to set a product name on the Consent screen; if so, click
    **Configure consent screen​** , supply the requested information, and click ​ **Save​** to return
    to the Credentials screen.
5. Select ​ **Web Application​** for the ​ **Application Type​**. Follow the instructions to enter
    redirect URIs, for our module redirect url is
    **{site-domain}/email_importer/index/gmailredirect/**
6. Click ​ **Create​**.
7. On the page that appears, copy the ​ **client ID​** and ​ **client secret​** to your clipboard.
![Credentails](/readme/Page-1-Image-2.png)
8. Goto ​magento admin >​config , select email importer config you will see fields for
    **client ID​** and ​ **client secret​** update your credentials save your config


## Create service gmail account

```
You need to ​create service account
```
## 1. From the Credentials page, click ​ Create credentials > OAuth client ID​ to

## create your OAuth 2.0 credentials or ​ Create credentials > Service account
![Credentails](/readme/Page-2-Image-3.png)

## key​ to create a service account.

## 2. If you created an OAuth client ID, then select your application type.

## 3. Fill in the form and click ​ Create​.
![Credentails](/readme/Page-2-Image-4.png)

## Generate a new access token for vendor gmail account

1. Goto ​magento admin >sales > dropship > ​Get Gmail Access Token
2. Login into single vendor email receiver account allow access for service created. it will
    redirect to our module page with token
    ![Credentails](/readme/Page-3-Image-5.png)    
3. Copy the token


## Set access token to gmail account for a vendor

1. On admin panel Goto magento admin > sales > dropship > vendors > select a vendor >
    select tab ​Preferences > on ​ **Email Stock Importer** ​section
2. you will find ​ **Gmail Importer Access Token** ​ field you can update it with gmail given
    token
3. Save vendor
