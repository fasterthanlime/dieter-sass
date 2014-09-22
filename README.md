# Dieter Sass

Compile your SASS/SCSS stylesheets into CSS via dieter.

Includes a vendored version of sass 3.4.5.

## Usage

In your project.clj file

[![Clojars Project](http://clojars.org/org.clojars.fasterthanlime/dieter-sass/latest-version.svg)](http://clojars.org/org.clojars.fasterthanlime/dieter-sass)

Insert it into your ring middleware stack

```clojure
(use '[dieter :only [asset-pipeline]])
(require 'dieter.asset.sass)

(-> app
    (asset-pipeline config-options))
```

## Upgrading sass

To update the version of sass bundled with this library, follow these step:

```sh
jruby -S gem install -i ./sass-gems sass --no-rdoc --no-ri 
jar cf sass-gems.jar -C sass-gems
```

Then put the resulting jar in `resources/vendor` of this repository.

**Note: this is mostly a self-reminder, as users of this library should
not have to upgrade sass on their own.**

## Credits

Based on [this old pull request](https://github.com/edgecase/dieter/pull/46) and
the [dieter-ember](https://github.com/edgecase/dieter-ember) plugin.

## License

Copyright (C) 2014 Amos Wenger

Distributed under the Eclipse Public License, the same as Clojure.
