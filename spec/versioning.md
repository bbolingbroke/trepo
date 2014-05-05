# Versioning
We use [semver](http://semver.org/) versioning.
See the home page for the current version.

# Header
Set the server version using the header `Accept-Version`.

You can read more about semver version syntax (such as  ~1.2.x) [here](https://www.npmjs.org/doc/misc/semver.html).

# Versioned Routes
// TODO explain this more clearly and make pictures.
Lets say route X (v1) was introduced in version 1.1.0 as a backward compatible route.
Eventually the overall version stands at 1.4.2, and we need to make a backwards compatible bug fix.
We update route X (to v2) with this change for all versions back to 1.1.0, and increment the overall version to 1.4.3.
Eventually the overall version stands at 1.5.7, and we need to make a backwards-incompatible change.
We upgrade route X (to v3) and the overall version number is now 2.0.0
Route X should now behave differently depending on the version.
If the requested version is greater than or equal to 1.1.0  and less than 2.0.0, we use v2.
If the requested version is 2.0.0 or greater, we use v3.
Later, we decide to retire route X when the overall version is 3.12.3.
Any request with version greater than or equal to 4.0.0 should return a 410 Route Deprecated.
Any request with version between 2.0.0 and 3.x.y should use v3.
Any request with version between 1.1.0 and 1.x.y should use v2. //FIX

# Deprecation
Routes that are deprecated return the status code `410 Gone` and a message stating when that version was deprecated.