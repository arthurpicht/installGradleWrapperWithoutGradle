# installGradleWrapperWithoutGradle

## How to install a gradle wrapper without gradle

***TLDR*** A bash script that installs a gradle wrapper in a java project
without a running gradle installation. Just copy script *create_gradle_wrapper.sh*
to the root of your project, make it executable and call it.

The [official gradle documentation](https://docs.gradle.org/current/userguide/gradle_wrapper.html#sec:adding_wrapper) states:

> To make the Wrapper files available to other developers and execution environments you’ll need to check them into version control. All Wrapper files including the JAR file are very small in size. Adding the JAR file to version control is expected. Some organizations do not allow projects to submit binary files to version control. At the moment there are no alternative options to the approach.

Well, I think, this is not entirely correct. Here is the solution:

1. Copy the script *create_gradle_wrapper.sh* to the root of your gradle
project and make it executable.

2. If you want your gradle wrapper to be pinned to a specific version,
declare the *gradle_version* variable in the first line of the script. Leave it commented to
get the latest version.

3. Call script.

As prerequesites *java* and *wget* must be installed.

And finally you should put the following lines to your *.gitignore* file:

    gradle/
    gradlew
    gradlew.bat

This script is based on a solution I found in the
[Lifeboat blog](http://blog.vorona.ca/init-gradle-wrapper-without-gradle.html). 
