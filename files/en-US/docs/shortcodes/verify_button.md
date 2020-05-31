# Verify Button

WP-WebAuthn provides multiple shortcodes that can be inserted into front-end pages to invoke the relevant function. The "Verify Button" is one of the shortcodes.

Use this short code to insert a test button into front-end pages that tests whether the current user's bound authenticator is working properly.

## Usage

```
[wwa_verify_button attribute="value"]
```

## Attributes

| Attribute | Values | Default | Description |
| ------------ | ------------- | ------------ | ------------ |
| display | `true`/`false` | `true` | Whether to display a short reminder for users who are not logged in. Set to `false` to hide it completely from unlogged users |

## Example

```
[wwa_verify_button display="false"]
```

!!! tip "Tip"
    Attributes are not required and default values will be used when no attribute value is specified. The order of the attributes also does not affect the final effect.

!!! tip "Style"
    The output button **DOES NOT** contain basic styles and you can write your own CSS rules.

!!! tip "Multiple buttons"
    Multiple buttons can be inserted per page without interfering with each other.