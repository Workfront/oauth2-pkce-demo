# OAuth2 PKCE Demo

Sample demo app that will let me understand how to connect to Workfront API with OAuth2 PKCE flow.
## Introduction

The OAuth Code Flow is one of the more typical and flexible token flows, and, with that, one of the most popular. The details of this flow are not covered by this article, but can be found in the [code flow overview](https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow-with-proof-key-for-code-exchange-pkce) article on the Curity Web site.

Proof Key for Code Exchange (PKCE) is a technique described in [RFC7636](https://tools.ietf.org/html/rfc7636), and is used to mitigate the risk of the authorization code being hijacked. More details on how to configure the Curity Identity Server to enable PKCE can be found in the [configuring PKCE in Curity](https://curity.io/resources/learn/pkce/) resource page.

The rest of this writeup explains how these technologies can be used in the JavaScript programming language. It is intentionally simple, so that the concepts are not obscured by superfluous details.

## Serving the Sample HTML File

The HTML needs to be served somehow from a Web server. Because the client is just a static HTML page, this can be done with a trivial server configuration. These are a couple of different ways to very easily server the static HTML page:

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

These will not use TLS, but are fast and easy ways to serve the HTML file without setting up any infrastructure