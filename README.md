# boot-rev

Boot task for file revisions (Naming files by version, hash etc.)

### Usage

in build.boot
```clj
(set-env! :dependencies '[[mrmcc3/boot-rev "0.1.0-SNAPSHOT"]])
(require '[mrmcc3.boot-rev :refer [rev]])

```

example

```clj
;; fingerprint all js files
(rev :files [#"^.*\.js$"])

;; you can get the reved path from the original path
(rev-path fileset "out/main.js") ;; -> out/main.ae34fc11.js
```

### LICENSE

Copyright © 2015 Michael McClintock

Distributed under the Eclipse Public License, the same as Clojure.
