django-oauth-access README
==========================

This app provides support for:

 * Twitter
 * LinkedIn
 * Yahoo
 * Facebook (using OAuth 2.0 — it is functional, but needs more work)
 * Likely any OAuth 1.0a compliant site

## Sample settings

Check sample_settings.py for examples of how to store your consumer keys.

## Callback View

On a successful signin with a service provider, you need to provide one / the same
view for each provider that looks like this:

    # views.py

    def oauth_access_success(request, access, token):
        access.persist() # stores the token in the database
        # do other stuff that I'll write about later
