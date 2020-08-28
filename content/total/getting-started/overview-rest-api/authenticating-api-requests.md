---
id: "authenticating-api-requests"
url: "total/authenticating-api-requests"
title: "Authenticating API Requests"
productName: "GroupDocs.Total Cloud"
weight: 1
description: ""
keywords: ""
---
There are two ways to authenticate GroupDocs for Cloud REST APIs.

1. OAuth 2.0
1. URL Signing

Though we are still supporting URL Signing, we recommend our users to switch to OAuth 2.0 as it is an industry standard and more convenient to use.

## OAuth 2.0 ##

The GroupDocs for Cloud REST API supports the OAuth 2.0 protocol using the **client_credentials** workflow to authorize calls.

[OAuth 2.0](https://en.wikipedia.org/wiki/OAuth#OAuth_2.0) is an authorization framework that enables applications to obtain access to user accounts data through our REST API. OAuth provides authorization flows for web and desktop applications, and mobile devices.

The basic concept and how it works is described in the next image:
![](total/images/gfc-oaut2.png)

## Applications ##

To access the REST API using OAuth2.0 protocol, you need to [create an application](https://docs.aspose.cloud/display/totalcloud/Create+New+App+and+Get+App+Key+and+SID). To register new applications, login into the [Dashboard Developer](https://dashboard.groupdocs.cloud) site using your GroupDocsAspose Account, and go to the [My Apps](https://dashboard.groupdocs.cloudapps) view. Once you create a new application, we will issue a **client_id** (App SID) and **client_secret** (App Key) that you can use to authenticate your REST API calls using the OAuth2.0 protocol. (You can generate new secrets for your Apps, but make sure you update it when issuing new access tokens using those credentials.)

## Get Access/Refresh Token ##

After you have created a new application you can obtain an access token by sending a **POST** request to **/oauth2/token** endpoint. Still, you must authenticate your access token request using Client Credentials authorization grant type flow:

```html
POST request to: https://api.groupdocs.cloud/oauth2/token
Headers:
  Accept: application/json
  Content-Type: application/x-www-form-urlencoded
  Body:
    grant_type: client_credentials
    client_id: APP_SID
    client_secret: APP_KEY
```

The endpoint acts as an authorization server and it verifies your credentials, if they are correct it returns a JSON ticket containing several items, through each, you can find the access_token, refresh_token, expire time of both tokens etc. The provided access_token is a Bearer Token that you can further use in the Authorization header of your request.

For each Application you create in the dashboard, you can only have one refresh_token in use for it. Any new request for refresh_token will override and revoke the previous one.

### cURL Example ###

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/oauth2/token" \
-X POST -d "grant_type#client_credentials&#x26;client_id#9b881efb-5e6c-428e-b65b-e05d37e15875&#x26;client_secret#98fb26e80f5614d029a312727136e041" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "access_token":"kZmTkha5y5VMJqH4DKIOPWrModatjNIMWxZkNvfIm65j62oLjjX4JhqiqnGf6wMvfKTB8ILAEs0F1SGnPDfTyGm2_jjq-jbyvNoEJGPzQyQSokalI9ufN3jIdxD-421io4BT2t4QQb8sq7FX8mVS5dKzh_SGZ3XNmbXmAMCL1wHcAjaTsvxp_sfrSpMeIdZ-pWZFdQS9wZePtWY1Ql2ZlIILwQCi5Wgm-vvsPHZv5qxRDbQxvmb0lidHvzzmopykqp7Mdgj9MkUWhax9Z4D1KSohknEsdte4pMEh3KforKbR7UL3lZIviVsc1Ef0AVWB5D26xdiKEZsTqL1sLXBpgSTzFeHMNMih6UYqWQqxpnySHG_bF95jHp8qgbjgMkEAc52NqKfwHDNNv1BzAGI3FFWCyTMKmtJv1mrcxN0e-P5Vldhp",
  "token_type":"bearer",
  "expires_in":86399,
  "refresh_token":"dc329902962f44b4b0108bef2818b0e2",
  "client_id":"9b881efb-5e6c-428e-b65b-e05d37e15875",
  "clientRefreshTokenLifeTimeInMinutes":"525600",
  ".issued":"Wed, 20 Dec 2017 06:23:32 GMT",
  ".expires":"Thu, 21 Dec 2017 06:23:32 GMT"
}
```

{{< /tab >}} {{< /tabs >}}

## Obtain new Access/Refresh Token using the Refresh Token ##

The access token is only valid for a small period of time, to continue to work with the REST API you can issue new access token by only using the refresh token provided at the above POST request. To obtain a new access token using the refresh token you can make a POST request to the same /oauth2/token endpoint but using different grant type this time:

  POST request to: https://api.groupdocs.cloud/oauth2/token
  Headers:
    Accept: application/json
    Content-Type: application/x-www-form-urlencoded
    Body:
      grant_type: refresh_token
      refresh_token: the-refresh-token-perviously-generated

The returned ticket will be the same as the above, but a new refresh_token is issued now and the old one is revoked, so make sure you replace it in your application with the new one from the ticket you just received.

### cURL Example ###

{{< tabs tabTotal="2" tabID="2" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/oauth2/token" \
-X POST \
-d "grant_type#refresh_token&#x26;refresh_token#dc329902962f44b4b0108bef2818b0e2" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
{
  "access_token":"_J7gynLXEsUVn8fCYlsHqP-Su6G3-TjRUQH328UFoMQ2j7wrh8_n5CcqqDU8Bpx7Pvkoc3I9K1AeDOINokG4a1pmXwfMdExQRt6vQ-356u-OQvZQjoYkDwNyEUObAlDbAw7LFcA1utZKnerf2JV6Q8Gjn00BH-N4IJaUY02jXzppPP7fOdx0RNTiUfAnAuemsDbItsyd-BTT8oIk2AwcTwIZM5ub5eFNYzgIrtrTDxVUMd6oG3-xAuGVM5h2Bc9D-G17pspaLXIEkeqyjSMaOzKHxi-vOUse3i8mRTNhu0gCHXt2q08MR_qMtfgGhT8ZQh-kk8bRTX9QVv-LzcSx7I0PTZkYM8Rha8QVr1aStXehlW2yIGo7YGQobeBnsn2zmIuR1CzczdxfePSQ4evPuoaSuFN9I9swLDFcZYfVdcq3Tk5i",
  "token_type":"bearer",
  "expires_in":86399,
  "refresh_token":"e74b3207c5594b82bddac0cf47967770",
  "client_id":"9b881efb-5e6c-428e-b65b-e05d37e15875",
  "clientRefreshTokenLifeTimeInMinutes":"525600",
  ".issued":"Wed, 20 Dec 2017 06:35:01 GMT",
  ".expires":"Thu, 21 Dec 2017 06:35:01 GMT"
}
```

{{< /tab >}} {{< /tabs >}}

## Call REST API ##

Now that you have the Bearer Token (access_token) generated using the application credentials, you can make API calls and authorize by adding the access token in the ‘Authorization’ header, as it’s defined in the OAuth 2.0 protocol.

```Headers: Authorization: Bearer ACCESS_TOKEN```

*You authorize with one application, but you can access files from all storages in your account, or all Application’s default storage by specifying query parameters (storage or AppSid).*

### cURL Example ###

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html
curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Freescale%20OSC.pdf/pages/1/resources/styles.css" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer _J7gynLXEsUVn8fCYlsHqP-Su6G3-TjRUQH328UFoMQ2j7wrh8_n5CcqqDU8Bpx7Pvkoc3I9K1AeDOINokG4a1pmXwfMdExQRt6vQ-356u-OQvZQjoYkDwNyEUObAlDbAw7LFcA1utZKnerf2JV6Q8Gjn00BH-N4IJaUY02jXzppPP7fOdx0RNTiUfAnAuemsDbItsyd-BTT8oIk2AwcTwIZM5ub5eFNYzgIrtrTDxVUMd6oG3-xAuGVM5h2Bc9D-G17pspaLXIEkeqyjSMaOzKHxi-vOUse3i8mRTNhu0gCHXt2q08MR_qMtfgGhT8ZQh-kk8bRTX9QVv-LzcSx7I0PTZkYM8Rha8QVr1aStXehlW2yIGo7YGQobeBnsn2zmIuR1CzczdxfePSQ4evPuoaSuFN9I9swLDFcZYfVdcq3Tk5i"
```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
    sup {
    top: -0.4em;
    vertical-align: baseline;
    position: relative;
  }
  sub {
    top: 0.4em;
    vertical-align: baseline;
    position: relative;
  }
  a:link { text-decoration:none; }
  a:visited { text-decoration:none; }

  @media screen and (min-device-pixel-ratio:0), (-webkit-min-device-pixel-ratio:0), (min--moz-device-pixel-ratio: 0) {
    .p1-EqxtBMuQ-view{ font-size:10em; transform:scale(0.1); -moz-transform:scale(0.1); -webkit-transform:scale(0.1); -moz-transform-origin:top left; -webkit-transform-origin:top left; } }
  .layer { }.ie { font-size: 1pt; }
  .ie body { font-size: 12em; }
  .p1-EqxtBMuQ-01 {
  position: absolute;
  white-space: nowrap;
  }
  .p1-EqxtBMuQ-02 {
    height: 66em;
    font-size: 1em;
    margin: 0em;
    line-height: 0.0em;
    display: block;
    border-style: none;
    width: 49.58333em;
  }
  @supports(-ms-ime-align:auto) { .p1-EqxtBMuQ-02 {width: auto; overflow: hidden;}}
    .p1-EqxtBMuQ-03 {
    position: relative;
  }
    .p1-EqxtBMuQ-04 {
    width: 100%;
    clip: rect(-0.041667em,49.625em,66.04166em,-0.041667em);
    position: absolute;
    pointer-events: none;
  }
  .p1-EqxtBMuQ-05 {
    position: relative;
    width: 49.58333em;
}
```

{{< /tab >}} {{< /tabs >}}

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}} {{< tab tabNum="1" >}}

```html

curl -v "https://api.groupdocs.cloud/v1/viewer/Test.msg/html/attachments/Freescale%20OSC.pdf/pages/1/resources/styles.css" \
-X GET \
-H "Content-Type: application/json" \
-H "authorization: Bearer _J7gynLXEsUVn8fCYlsHqP-Su6G3-TjRUQH328UFoMQ2j7wrh8_n5CcqqDU8Bpx7Pvkoc3I9K1AeDOINokG4a1pmXwfMdExQRt6vQ-356u-OQvZQjoYkDwNyEUObAlDbAw7LFcA1utZKnerf2JV6Q8Gjn00BH-N4IJaUY02jXzppPP7fOdx0RNTiUfAnAuemsDbItsyd-BTT8oIk2AwcTwIZM5ub5eFNYzgIrtrTDxVUMd6oG3-xAuGVM5h2Bc9D-G17pspaLXIEkeqyjSMaOzKHxi-vOUse3i8mRTNhu0gCHXt2q08MR_qMtfgGhT8ZQh-kk8bRTX9QVv-LzcSx7I0PTZkYM8Rha8QVr1aStXehlW2yIGo7YGQobeBnsn2zmIuR1CzczdxfePSQ4evPuoaSuFN9I9swLDFcZYfVdcq3Tk5i"

```

{{< /tab >}} {{< tab tabNum="2" >}}

```html
  sup {
  top: -0.4em;
  vertical-align: baseline;
  position: relative;
}
sub {
  top: 0.4em;
  vertical-align: baseline;
  position: relative;
}
a:link {text-decoration:none;}
a:visited {text-decoration:none;}
@media screen and (min-device-pixel-ratio:0), (-webkit-min-device-pixel-ratio:0), (min--moz-device-pixel-ratio: 0) {.p1-EqxtBMuQ-view{ font-size:10em; transform:scale(0.1); -moz-transform:scale(0.1); -webkit-transform:scale(0.1); -moz-transform-origin:top left; -webkit-transform-origin:top left; } }
.layer { }.ie { font-size: 1pt; }
.ie body { font-size: 12em; }
.p1-EqxtBMuQ-01 {
  position: absolute;
  white-space: nowrap;
}
.p1-EqxtBMuQ-02 {
  height: 66em;
  font-size: 1em;
  margin: 0em;
  line-height: 0.0em;
  display: block;
  border-style: none;
  width: 49.58333em;
}
@supports(-ms-ime-align:auto) { .p1-EqxtBMuQ-02 {width: auto; overflow: hidden;}}
  .p1-EqxtBMuQ-03 {
  position: relative;
}
.p1-EqxtBMuQ-04 {
  width: 100%;
  clip: rect(-0.041667em,49.625em,66.04166em,-0.041667em);
  position: absolute;
  pointer-events: none;
}
.p1-EqxtBMuQ-05 {
  position: relative;
  width: 49.58333em;
}
```

{{< /tab >}} {{< /tabs >}}

## Tokens Lifetime ##

The time of the tokens is finite. By default, the **access_token** lifetime is **1 day**, and the **refresh_token** lifetime is **1 year**. Before you create a new access_token, use it and renew it only before it expires. To detect when an access token expires, you must write specific code that will check for any of these:

* **expires_in** value in the ticket generated by OAuth2 endpoint.
* will handle the **401 Unauthorized** error responses from the API endpoint and issue a request for a new token.

## URL Signing ##

Each GroupDocs for Cloud API request must include the following query string parameters:

| Parameter | Description
|---|---
|**appSID**|The public key provided to a client that allows the GroupDocs API to know which client is making the API request
|**signature**|A HMAC-SHA1 signature of the request that is generated by the client using their private key

## How to authenticate (URL Signing) ##

GroupDocs for Cloud uses URL signing for authorization of requests. All requests sent to the GroupDocs for Cloud Web Service must be signed using user's private key which they retrieve via the Web UI when they sign up. Using the Private key ensures that only authorized application can create valid REST requests to our Web API.

Please take following steps to generate a valid signature (as an example we are using `appSID#c821f123-1a8b-4b97-925a-9d69a6b2fcd8 and key#23e9d89a967a5f18142221fa8f7cbcd0`):

1. Build the URL which requires to be signed including all parameters. [https://api.groupdocs.com/v1/storage/folder/test_folder](https://api.groupdocs.com/v1/storage/folder/test_folder)
1. Remove trailing '/' character if any.
1. Append App SID to the given URL as query parameter [http://api.groupdocs.com/v1/storage/folder/test_folder?appSID#c821f123-1a8b-4b97-925a-9d69a6b2fcd8](https://api.groupdocs.com/v1/storage/folder/test_folder?appSID#c821f123-1a8b-4b97-925a-9d69a6b2fcd8)
1. Use HMAC-SHA1 algorithm to compute the hash of the URL. App Key will be used as a secret cryptographic key.
1. Use Base64 encoding to convert message authentication code (MAC) from a binary format in an ASCII string format. `JgLReiOyORY8BYpCJ32CbCc0UHg#`
1. Remove any trailing '#' characters: `JgLReiOyORY8BYpCJ32CbCc0UHg`
1. URL-encode generated string: `JgLReiOyORY8BYpCJ32CbCc0UHg`. This step encodes the string to be used in a query part of a URL.
1. Finally, append the encoded value to the URL as a signature parameter.[http://api.groupdocs.com/v1/storage/folder/test_folder?appSID#c821f123-1a8b-4b97-925a-9d69a6b2fcd8&signature#JgLReiOyORY8BYpCJ32CbCc0UHg](http://api.groupdocs.com/v1/storage/folder/test_folder?appSID#c821f123-1a8b-4b97-925a-9d69a6b2fcd8&signature#JgLReiOyORY8BYpCJ32CbCc0UHg)

{{< alert style="info" >}}
We didn't use registered application ID and application key here, so the resulting URL does not pass authorization but all calculationwerecompleted using the real algorithm, so you can use the results for internal testing.
{{< /alert >}}

See below implementation of the URL signing algorithm in different languages.

{{< tabs tabTotal="1" tabID="5" tabName1="C#" >}} {{< tab tabNum="1" >}}

{{< gist groupdocscloud caf8bcd223759d65afaa07436f251820 Viewer_CSharp_Signing_URL.cs >}}

{{< /tab >}} {{< /tabs >}}
