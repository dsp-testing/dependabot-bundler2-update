# dependabot-bundler2-update

This scenario currently doesn't work in dependabot-core.

`Gemfile.lock` has been bundled with bundler 2.1.4, byebug 11.0.0 is installed that requires bundler v2 so we should propose an update to byebug.

Test this update in dependabot-core:

```
bin/dry-run.rb bundler dsp-testing/dependabot-bundler2-update --cache=files --dep=byebug
```

Expected output:

```
=== byebug (11.0.0)
 => checking for updates 1/1
 => latest available version is 11.1.3
 => latest allowed version is 11.1.3
 => requirements to unlock: own
 => requirements update strategy: bump_versions
 => updating byebug from 11.0.0 to 11.1.3

    ± Gemfile
    ~~~
    6c6
    < gem "byebug", "~> 11.0.0"
    ---
    > gem "byebug", "~> 11.1.3"
    ~~~

    ± Gemfile.lock
    ~~~
    4c4
    <     byebug (11.0.0)
    ---
    >     byebug (11.1.3)
    11c11
    <   byebug (~> 11.0.0)
    ---
    >   byebug (~> 11.1.3)
    ~~~
 ```
