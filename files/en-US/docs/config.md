# Installation & Configuration

## Installation

You can search and install WP-WebAuthn from [WordPress plugin directory](https://wordpress.org/plugins/wp-webauthn/) in the dashboard. This is the recommended installation method.

You can also download and install from [GitHub Releases](https://github.com/yrccondor/wp-webauthn/releases).

## Configuration

After activation, WP-WebAuthn will attempts to automatically configure all options to the appropriate values, but you'd better head over to the settings page to check it out.

Plugin settings are only displayed to administrators with `edit_plgins` permissions. The register authenticator form, the list of registered authenticators and the verify login button are displayed to all logged-in users.

The descriptions for plugin settings are as follows:

- **Preferred login method**: Configure the default login method for the login page.

- **Website identifier**: Passed to the browser during the WebAuthn authentication process for user recognition. May not be displayed depending on the browser policy.

- **Website domain**: Must be exactly the same with the current domain or parent domain.

- **Require user verification**: User authentication is a feature in WebAuthn that can improve the security of WebAuthn to some extent, but some mobile devices do not support this feature well. If you are having trouble when registering authenticators or loging-in, you can try to disabling user authentication.

- **Allow to login without username**: Userless login is a feature in WebAuthn that allows users to log into the correct account without entering a username. Requires authenticator and browser support.

- **Logging**: When enabled, administrators with `edit_plgins` permissions can see a log output box to view plugin logs for debuging. Enabling this option will reduce plugin's performance, so enable it only when needed.