### Authentication

Currently we only support Client-side Flow. We plan to support Server-side Flow in the future. No plan for implementing Password Flow.

(Following borrowed from [appdotnet api-specs](https://github.com/appdotnet/api-spec/blob/master/auth.md))

#### Client-side Flow

If you're building a client-side Javascript app or a mobile app that doesn't have an associated back-end server, you'll find that you need to take some special steps to keep your `client_secret` confidential.

1. Direct the user that you want to authenticate to this URL:
    ```
    https://molis-tld.com/oauth/authenticate
        ?client_id=[your client ID]
        &response_type=token
        &redirect_uri=[your redirect URI]
        &scope=[scopes separated by spaces]
    ```

    > To avoid cross-site scripting attacks, we also support the **state** parameter. If you include a state parameter, we will append it to the query parameters when redirecting the user to your **Redirection URI**.

    > To comply with Apple's App Store Guidelines, you can add the query string parameter ```adnview=appstore``` to hide all signup links on the authentication pages.

    We'll request that the user log in to App.net and show them a permissions dialog allowing them to choose whether to authorize your application.

1. If the user decides to authorize your application, they will be redirected to:
    `https://[your registered redirect URI]/#access_token=[user access token]`

    > If you included a query string in your redirect URI, the `code` parameter will be appended. Likewise, the scheme of your redirect URI will be respected, though we strongly recommend sending all traffic over HTTPS.

    The access_token will be appended to the URI in the fragment section, encoded as if it were a query string. Your client-side code should parse this for the access_token.