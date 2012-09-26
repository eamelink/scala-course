Hands on Play 2
===============

Installation of Play 2
----------------------

Play 2 is an SBT Plugin; so if you have SBT you don't need to download Play 2 to run a Play 2 project. However, Play 2 is built for a specific version of SBT (0.11.2), and won't work with the most recent SBT (0.12.0). If you use the 'advanced' SBT launcher that detects versions, this is not a problem, but if you use the 'dumb' SBT launcher (on Windows), you'll need the proper SBT version.

In both cases; this will only help you if you already have a Play 2 project, which you may not. To create a new Play 2 project, having Play 2 itself installed is the easiest way. So:

 * Download Play 2.0.3 from [Playframework.org](http://www.playframework.org)

Getting Started
---------------

 * Run `play new` to create a new Play project, choose "Create a simple Scala application"
 * `cd` into the directory and run `play`
 * Run `eclipsify` to create an Eclipse project, and import into Eclipse
 * Optional: Make Eclipse automatically refresh: Preferences -> General -> Workspace -> Refresh using native hooks or polling
 * Run `~run` to run the application, and recompile automatically when the sources change

Exercise
--------

Create a Play 2 application that does the following:
 
 * Shows a form with a single text field: search
 * On submit, validates that it starts with `@` or `#`
 * Does a Twitter search API request searching for five tweets with this username or hashtag
 * Shows the results

Hints
-----
 
General hint: [The Play 2 Scala documentation](https://github.com/playframework/play20/wiki/Scalahome) and [Scaladoc](http://www.playframework.org/documentation/api/2.0.3/scala/index.html#package)

### Showing the form

You'll need to create a [Controller and Action](https://github.com/playframework/Play20/wiki/ScalaActions) and a [Route](https://github.com/playframework/Play20/wiki/ScalaRouting)

You'll need a [template](https://github.com/playframework/Play20/wiki/Scalatemplates) and a [Form](https://github.com/playframework/Play20/wiki/ScalaForms)

### Validating the form

See the [Form](https://github.com/playframework/Play20/wiki/ScalaForms) documentation.

### Do a Twitter search

The [Twitter Search API](https://dev.twitter.com/docs/api/1/get/search) doesn't need authentication. Use the [WS API](https://github.com/playframework/Play20/wiki/ScalaWS) to access it.

### Show the results

The Twitter response is JSON, you'll need to parse the response with Play's [JSON API](https://github.com/playframework/Play20/wiki/ScalaJson). It's useful to create a [Scala Case Class](http://www.scala-lang.org/node/107) to represent a Tweet.

