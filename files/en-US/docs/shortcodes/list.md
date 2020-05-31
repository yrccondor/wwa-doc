# Authenticator List

WP-WebAuthn provides multiple shortcodes that can be inserted into front-end pages to invoke the relevant function. The "Authenticator List" is one of the shortcodes.

Use this short code to insert the a list of bound authenticators of current user into front-end pages with renaming and removal operations.

## Usage

```
[wwa_list attribute="value"]
```

## Attributes

| Attribute | Values | Default | Description |
| ------------ | ------------- | ------------ | ------------ |
| display | `true`/`false` | `true` | Whether to display a short reminder for users who are not logged in. Set to `false` to hide it completely from unlogged users |

## Example

```
[wwa_list display="false"]
```

!!! tip "Tip"
    Attributes are not required and default values will be used when no attribute value is specified. The order of the attributes also does not affect the final effect.

!!! tip "Style"
    The output form contains basic styles and you can write your own CSS rules.

!!! info "Data update"
    The data in the list will be automatically updated. If there is a register form on the page, the action of registering an authenticator also causes the list to update automatically.

!!! tip "Multiple lists"
    Multiple lists can be inserted per page and all data is updated synchronously.