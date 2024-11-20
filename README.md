# country-wise-content-on-cache
This gist has the logic to show the country wise content on the pages if the cache is enabled on the site and users are getting version

# Problem
1. When using cache plugins like Autoptimize, WPOptimize or any caching plugin if you have multi-country products once the page is cached in any country it shows the same content everywhere to every country user.
E.G. I have a page with products showing in multiple countries. Products have different pricing for every country type. If cache is enabled if a user accesses a site from Singapore the page gets cached, user can see the current countr wise product but because of the cached version of the page the user in India also gets the singapore's version of site.

# Solution
We will load the country wise content using javascript. We will fetch the country details using the Javscript API of any API service, The after getting the responses we will hide/show/replace the content on the Client. This solution works because The cached version is fetched from the server hence it is cached. If the content is manipulated on Client side it will not cache the Javascript requests and on every hit we will get the correct country code and hence can hide/show/replace the content on the page. Shortcodes also gets cached hence using JS it works.
