CloudFoundry Test Buildpack
===========================

This is a simple build pack that just dumps information about the build pack environment, in particular during the compile process.

Usage
-----

1. Create a project folder and execute ```touch cache-test.txt``` inside that folder.  This file must exist or the test build pack will skip processing.

2. In the project directory, execute this command.

```
cf push --buildpack=https://github.com/dmikusa-pivotal/cf-test-buildpack.git
```

3. You should see a bunch of information about the environment dumped to the screen during the compile phase.

4. If you go to the URL for your application, there is a basic HTTP file server running which allows you to further explore the environment.

