# Adobe Workfront OAuth2 PKCE Demo

Sample demo app that will let you understand how to connect to Adobe Workfront API through OAuth2 PKCE flow.

## Introduction

Proof Key for Code Exchange (PKCE) is a technique described in [RFC7636](https://tools.ietf.org/html/rfc7636), and is used for SPA or native apps. More details on how to configure the OAuth2 application for PKCE can be found in the [Create an OAuth2 single-page web application using PKCE](https://one.workfront.com/s/document-item?bundleId=the-new-workfront-experience&topicId=Content%2FAdministration_and_Setup%2FConfigure_integrations%2Fcreate-oauth-application.htm&_LANG=enus) page.

More details on how the PKCE flow works can be found in article: [Configure and use your organization’s custom OAuth 2 applications using PKCE flow](https://one.workfront.com/s/document-item?bundleId=the-new-workfront-experience&topicId=Content%2FWF_API%2FAPI%2Foauth-app-pkce-flow.htm&_LANG=enus)



## Serving the Sample HTML File

The HTML needs to be served somehow from a Web server. Because the client is just a static HTML page, this can be done with a trivial server configuration. Bellow are a couple of different ways to very easily server the static HTML page. 

NOTE: you can use your own way of searching HTML or even copy the JS function to your own web application. This page is just for educational proposes.

```sh
$ npx http-server -p <port>
```

```sh
$ php -S <host>:<port>
```

```sh
Python 2 — $ python -m SimpleHTTPServer <port>
Python 3 — $ python -m http.server <port>
```

## Update HTML file
 - Update HTML file to set right clientID that you have created by following steps in the article [Create an OAuth2 single-page web application using PKCE](https://one.workfront.com/s/document-item?bundleId=the-new-workfront-experience&topicId=Content%2FAdministration_and_Setup%2FConfigure_integrations%2Fcreate-oauth-application.htm&_LANG=enus)
 - Make sure the client APP you have created in Workfront has the right redirect URL of the page where you serve this html
 
 NOTE: localhost cannot be used as a valid redirect URL, if you don't have an externally available host, you can use Ngrok.

