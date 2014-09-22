# Dieter Sass

Compile your SASS/SCSS stylesheets into CSS via dieter.

Includes a vendored version of sass 3.4.5.

## Usage

In your project.clj file

    [dieter/sass "0.0.1"]

Insert it into your ring middleware stack

```clojure
(use '[dieter :only [asset-pipeline]])
(require 'dieter.asset.sass)

(-> app
    (asset-pipeline config-options))
```

## Credits

Based on [this old pull request](https://github.com/edgecase/dieter/pull/46) and
the [dieter-ember](https://github.com/edgecase/dieter-ember) plugin.

## License

Copyright (C) 2014 Amos Wenger

Distributed under the Eclipse Public License, the same as Clojure.
