# Register Form

WP-WebAuthn provides multiple shortcodes that can be inserted into front-end pages to invoke the relevant function. The "Register Form" is one of the shortcodes.

Use this short code to insert the authenticator register form into front-end pages.

## Usage

```
[wwa_register_form attribute="value"]
```

## Attributes

| Attribute | Values | Default | Description |
| ------------ | ------------- | ------------ | ------------ |
| display | `true`/`false` | `true` | Whether to display a short reminder for users who are not logged in. Set to `false` to hide it completely from unlogged users |

## Example

```
[wwa_register_form display="false"]
```

!!! tip "Tip"
    Attributes are not required and default values will be used when no attribute value is specified. The order of the attributes also does not affect the final effect.

!!! tip "Style"
    The output form contains basic styles and you can write your own CSS rules.

!!! danger "Multiple forms"
    Only one register form can be inserted per page, otherwise it may cause errors.