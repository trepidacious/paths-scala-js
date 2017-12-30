Paths.scala.js
==============

[Paths.js](https://github.com/andreaferretti/paths-js) is a library to generate [SVG paths](http://www.w3.org/TR/SVG/paths.html), allowing you to create your own charts using a functional and testable API. Paths.scala.js is the binding of Paths.js for [Scala.js](http://www.scala-js.org/).

This is an updated fork based on [csar's fork](https://github.com/csar/paths-scala-js) to update versions, in particular to scala 2.12.4 and scala-js 0.6.21.

Documentation
-------------

The usage of Paths.scala.js is mostly similar to its parent library. You can

- browse the [documentation of Paths.js](https://github.com/andreaferretti/paths-js/wiki)
- explore the [Scaladocs API](http://andreaferretti.github.io/paths-scala-js)
- see an [example application](https://github.com/andreaferretti/paths-scala-js-demo) ([live demo](http://andreaferretti.github.io/paths-scala-js-demo/))

The demo application is still incomplete, and fails to show many of Paths.scala.js features. The [Paths.js demo](http://andreaferretti.github.io/paths-js-demo/) better showcases what can be done.

Usage
-----

First you will need to run `sbt publishLocal`. Then in a Scala.js project, you can depend on Paths.scala.js with

    libraryDependencies += "org.rebeam" %%% "paths-scala-js" % "0.4.5"

Compatibility
-------------

Paths.scala.js is meant to have an API that is exactly equivalent to its parent library. The only exception is in the `Graph` and `Sankey` charts, where instead of accepting a parameter `data` with `nodes` and `links` fields, the Scala.js API directly requires `nodes` and `links` parameters. This removes one level of nesting and eliminates the need for structural typing in this particular case.

Please, file any other incompatibility between Paths.js and Paths.scala.js as an issue.