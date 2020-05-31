# FAQ

## Download

> Where can I get WP-WebAuthn?

You can search and install WP-WebAuthn from [WordPress plugin directory](https://wordpress.org/plugins/wp-webauthn/) in the dashboard.

WP-WebAuthn is open-sourced on [Github](https://github.com/yrccondor/wp-webauthn), you can help us to improve WP-WebAuthn.

## Usage

> I didn't purchase an authenticator like Yubikey, can I use WebAuthn?

Yes! WebAuthn supports authenticators more than just USB keys. On Windows, you can use Windows Hello to authenticate by facial recognition, fingerprint recognition or enter a PIN to authenticate; on Android, you can use fingerprint recognition, iris scan or enter the lock screen password to authenticate; on MacOS, you can scan your fingerprint to authenticate.

In these cases, it is your device that replaced your password and there is no need to worry about security.

> WP-WebAuthn doesn't seem to be working properly, what should I do?

WebAuthn requires a secure context to be called up properly, that is, your site needs to use HTTPS, or be in `localhost`.

In addition, WP-WebAuthn requires two PHP extensions, gmp and mbstring. These two extensions are not installed by default and you need to check them yourself.

If you still run into issues, you can go to our [Github repository](https://github.com/yrccondor/wp-webauthn) and submit an [issue](https://github.com/yrccondor/wp-webauthn/issues) **with a plugin log that could reproduce the issue.**

> What is user verification? Should I enable it?

If user verification is enabled, the plugin will require the authenticator to verify that "user is verified" but not just "user is present". Authentication methods may vary depending on the platform and authenticator, common methods include entering a PIN, entering a password, etc. Since many devices do not support user verification and user verification is actually performed in different ways, user verification can only improve the security of authentication in some cases.

If you don't have high requirements for login security, you can disable user verification.

> What is the principle of usernameless authentication? Can I enable it?

If userless authentication is enabled, the authenticator will store the user ID and bind it to the login credentials when the authenticator is registered. When logging in, there is no need to enter a user name; WP-WebAuthn will look for the user through the user ID sent by the authenticator and verify the login credentials. This process is secure.

Since authenticators will permanently store information such as user IDs in their built-in storage during this process, the number of userless login credentials that a single authenticator can register is limited. For Yubikey, this is usually 25. However, you can clear the credentials stored in the authenticator by resetting it.

You should only register an authenticator with userless login enabled if you feel it is necessary to use the userless login feature.

## Develop

> Can I modify WP-WebAuthn?

Yes, WP-WebAuthn is open-sourced using the GPL-3.0 licence, and you can modify the plugin if you like, but you must obey the GPL-3.0 licence.

If you find your modification is helpful to others, please consider to submit a [Pull Request](https://github.com/yrccondor/wp-webauthn/pulls) to us.

## Other Questions

> I'm having trouble using WP-WebAuthn, what should I do?

Find or submit an [issue](https://github.com/yrccondor/wp-webauthn) in our [Github repository](https://github.com/yrccondor/wp-webauthn/issues), and if you plan to submit an issue, **be sure to include a plugin log that could reproduce the issue.**

> How to ask questions properly?

Please refer to [How To Ask Questions The Smart Way](http://www.catb.org/~esr/faqs/smart-questions.html).

> What should I do if I believe WP-WebAuthn is unusable and is like rubbish?

I agree.