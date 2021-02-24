# dependabot-bundler2-update

This scenario currently doesn't work in dependabot-core.

`Gemfile.lock` has been bundled with bundler 2.1.4, guard-bundler 2.2.1 is installed that requires bundler v1 so we should propose an update to guard-bundler 3.0.0.

Test this update in dependabot-core:

```
bin/dry-run.rb bundler dsp-testing/dependabot-bundler2-update --cache=files --dep=guard-bundler
```
