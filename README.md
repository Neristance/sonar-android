sonar-android-lint-plugin
=========================

### Adaptions

In order to have the 220 Lint rules (status 28th September 2015), this project was forked and adapted, to build the project it might be necessary to skip test, because they were not updated.

### Build status

[![Build Status](https://api.travis-ci.org/SonarCommunity/sonar-android.png)](https://travis-ci.org/SonarCommunity/sonar-android)

<img src="https://raw.github.com/SonarCommunity/sonar-android/master/logo-sonar-android-lint-plugin.png" width="300" height="359"/>

See http://docs.codehaus.org/display/SONAR/Android+Plugin


**Contributions are welcome. Join the effort !**

Extension plugin for Android Lint in Sonar.

The idea is to visualize Android Lint errors directly in Sonar, in the same way as findbugs / PMD / checkstyle errors are reported.

I - Compiling and Installing the plugin:
---------------------------------------
 - Install maven
 - Clone the repository
 - Compile and test the code, then generate the jar:
	-> run "mvn clean install" command in your terminal
 - copy the jar (in the new generated target folder) in <path_to_your_sonar_install>/extensions/plugins folder,
 - restart sonar

II - Running an analyse:
------------------------
1. On a Maven project
 - mvn sonar:sonar -Dsonar.profile="Android Lint" in your project

2. On another project using sonar-runner
 - Add this property to your sonar-project.properties
  -> sonar.profile=Android Lint
