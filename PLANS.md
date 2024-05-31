# Plans

## Version 2.0

A new modular `Auth\Core` class will replace `Auth\Simple`, and will have some
functionality currently in the `Lum\Controllers\Auth` trait (see `lum-app`),
including `get_auth()`, and parts of `get_user()` and `set_user()`.

The password-checking stuff split into a new `Plugins\Password` plugin class.

The `Plugins\IPAccess` plugin will be updated to require an underlying user.

A bunch of the stuff currently in `Models\Common\Auth_Token*` will be moved
into an `Auth\Tokens` utility class so that the actual token parsing 
is handled here. Implementing long-planned token formats while I'm at it.

