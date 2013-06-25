CloudFoundry Caching Test Buildpack
===================================

This is a simple build pack that was written to test the capabilities of the cache directory, which is the second parameter passed to the ```bin/compile``` script.


Expected Behavior
-----------------

As indicated [here](https://groups.google.com/a/cloudfoundry.org/forum/#!topic/vcap-dev/1c0TvJfjCOw).

"My understanding is that as currently implemented, the buildpack cache is for the lifetime of the application guid and does not have a size limit. It's only used during the buildpack compile process and is scoped to the application guid, not to the buildpack.

So if you push an app with the same app GUID (which is triggered by pushing an app with the name of an app that already exists in a targeted space), then the cache will be downloaded from the cloud controller blob store and made available to the buildpack compile process in the Warden container. If you want to delete the cache, currently you have to delete the application and repush it to start with an empty cache.

We realized during the implementation that having an unbounded cache is a not ideal and have work identified to address that.

We have a team that is working a lot with a Java buildpack and they believe that having a cache that is shared per-buildpack could be useful. We have not made final decisions about caching and buildpacks. Certainly there are additional improvements and optimizations to make."


Results
-------

Still a work in progress.
