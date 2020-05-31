# Login Form

WP-WebAuthn provides multiple shortcodes that can be inserted into front-end pages to invoke the relevant function. The "Login Form" is one of the shortcodes.

Use this short code to insert the WebAuthn login form into front-end pages.

## Usage

```
[wwa_login_form attribute="value"]
```

## Attributes

| Attribute | Values | Default | Description |
| ------------ | ------------- | ------------ | ------------ |
| traditional | `true`/`false` | `true` | Contain traditional username+password login form |
| username | Any string | *Empty* | Default username in the form |
| auto_hide | `true`/`false` | `true` | Automatically hide from logged-in users |
| to | Any string | *Empty* | The URL of the page you turn to after a successful login, must be a absolute path. If left blank, you will go to the original page where the login was initiated |

## Example

```
[wwa_login_form traditional="false" to="https://flyhigher.top/"]
```

!!! tip "Tip"
    Attributes are not required and default values will be used when no attribute value is specified. The order of the attributes also does not affect the final effect.

!!! tip "Style"
    The output form contains basic styles and you can write your own CSS rules.

!!! danger "Multiple forms"
    Only one login form can be inserted per page, otherwise it may cause errors.
