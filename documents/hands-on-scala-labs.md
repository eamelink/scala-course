Getting started with the Scala Labs
===================================

The Scala-Labs are a set of exercises for Scala, developed by Xebia. They consist of code with failing tests and your job is to make the tests pass. Solutions are also provided.

Downloading
-----------

 * `git clone https://github.com/eamelink/scala-labs.git`

Eclipsify'ing
-------------

 * `cd scala-labs/labs`
 * `sbt eclipse`
 * Import the project into Eclipse with File -> Import -> Existing projects into workspace

Running
-------

What you run is the tests. To avoid running all the tests while you're just working on a single labs, use the following:

 * `sbt`
 * When in the SBT console, run `test-only org.scalalabs.basic.lab01.*`
 * On a fresh clone, this should report 4 failures

You can also prefix this command with a `~`, to have it executed after every source change.

Solving the problems!
---------------------

Start by reading the `src/test/scala/org/scalalabs/basic/lab01/HelloWorldExerciseTest.scala` and fix the Scala code in `src/main/scala/org/scalalabs/basic/lab01`