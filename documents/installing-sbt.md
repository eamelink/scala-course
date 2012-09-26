Installing SBT
==============

For Linux / OS X users
----------------------

You are lucky.

 * Download https://github.com/paulp/sbt-extras/blob/master/sbt, save it into ~/bin and make it executable.
 * Create a file ~/.sbt/0.12.0/plugins/plugins.sbt, with the following content:

   `addSbtPlugin("com.typesafe.sbteclipse" % "sbteclipse-plugin" % "2.1.0")`

You now have an advanced SBT launcher script, that can detect the proper SBT version for your project, and download it for you. 

For Windows users
-----------------

If you have Cygwin, you are lucky, you should be able to use the Linux / OS X instructions above.

If you don't have Cygwin, you're not lucky, but here goes:

 * Install SBT from the MSI on https://github.com/harrah/xsbt/wiki/Getting-Started-Setup
 * Create a file ~/.sbt/plugins/plugins.sbt, with the following content:

   `addSbtPlugin("com.typesafe.sbteclipse" % "sbteclipse-plugin" % "2.1.0")` 

You now have a dumb SBT launcher script, that will only work for the SBT version that you intalled.