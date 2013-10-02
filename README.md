# Dashing Travis CI Widget

## Description

Simple [Dashing](http://shopify.github.com/dashing) widget to display the
status of the latest build for a repository.

## Dependencies

[travis](https://github.com/travis-ci/travis)

Add it to your dashing's Gemfile.

```ruby
gem "travis"
```

## Configuration

The Travis CI job expects `config/travisci.yml` that looks like:

```yaml
org:
  auth_token: my_org_auth_token
  repositories:
    ci_travis_radar: zendesk/radar
  type: org
pro:
  auth_token: my_pro_auth_token
  repositories:
    ci_travis_radar: zendesk/zendesk
  type: pro
```

`repositories` is an hash of repositories and the keys (eg. `ci_travis_radar`) map to a dashing data-ids.  `type` selects whether or not to use a `pro` travis account.

To include the widgets in a dashboard, add the following snippet to the
dashboards layout file:

```html
<li data-row="1" data-col="1" data-sizex="1" data-sizey="1">
  <div data-id="ci_travis_radar" data-view="Travis" data-unordered="true" data-title="Radar"></div>
</li>

<li data-row="1" data-col="1" data-sizex="1" data-sizey="1">
  <div data-id="ci_travis_zendesk" data-view="Travis" data-unordered="true" data-title="Zendesk"></div>
</li>
```

## Preview

![Preview](https://s3.amazonaws.com/zendesk-github/dashing_travisci/dashing_travisci.png)

## Contributors

Elliot Pahl, Zendesk  
Jason Smale, Zendesk

## Copyright and license

Copyright 2013 Zendesk

Licensed under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations under
the License.
