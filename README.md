# SmallRye Code Rules
Code rules for SmallRye project family. 

## Contributing

**Want to contribute? Great!** 
We try to make it easy, and all contributions, even the smaller ones, are more than welcome.
This includes bug reports, fixes, documentation, examples... 
But first, read this page (including the small print at the end).

## Legal
All original contributions to SmallRye are licensed under the [ASL - Apache License](https://www.apache.org/licenses/LICENSE-2.0), version 2.0 or later, or, 
if another license is specified as governing the file or directory being modified, such other license.

All contributions are subject to the [Developer Certificate of Origin (DCO)](https://developercertificate.org/).
The DCO text is also included verbatim in the [dco.txt](dco.txt) file in the root directory of the repository.

## Reporting an issue
The SmallRye projects use GitHub to manage the issues. Open an issue directly at the project's GitHub page.

If you believe you found a bug, and it's likely possible, please indicate a way to reproduce it, what you are seeing and what you would expect to see.
Don't forget to indicate your SmallRye, Java, Maven and other relevant versions. 

## Before you contribute
To contribute, use GitHub Pull Requests, from your **own** fork.

### Code reviews
All submissions, including submissions by project members, need to be reviewed before being merged.

### Continuous Integration
Because we are all humans, the project uses a continuous integration approach and each pull request triggers a full build.
Please make sure to monitor the output of the build and act accordingly.

### Tests and documentation are not optional
Don't forget to include tests in your pull requests. 
Also don't forget the documentation (reference documentation, javadoc...).

## Setup
If you have not done so on this machine, you need to:
 
* Install Git and configure your GitHub access
* Install Java SDK (OpenJDK recommended)
* Clone the SmallRye project from your previously created fork

### IDE Config and Code Style
SmallRye has a strictly enforced code style. Code formatting is done by the Eclipse code formatter, using the config files
found in the [src/main/resources/io/smallrye/coderules](src/main/resources/io/smallrye/coderules) directory. 
By default when you run `mvn install` the code will be formatted automatically.
When submitting a pull request the CI build will fail if running the formatter results in any code changes, so it is
recommended that you always run a full Maven build before submitting a pull request.

If you want to run the formatting without doing a full build, you can run `mvn process-sources`.

#### Eclipse Setup
Open the *Preferences* window, and then navigate to _Java_ -> _Code Style_ -> _Formatter_. Click _Import_ and then
select the [src/main/resources/io/smallrye/coderules/eclipse-format.xml](src/main/resources/io/smallrye/coderules/eclipse-format.xml) file in the [src/main/resources/io/smallrye/coderules](src/main/resources/io/smallrye/coderules) directory.

Next navigate to _Java_ -> _Code Style_ -> _Organize Imports_. Click _Import_ and select the [src/main/resources/io/smallrye/coderules/eclipse.importorder](src/main/resources/io/smallrye/coderules/eclipse.importorder) file.

#### IDEA Setup
Open the _Preferences_ window, navigate to _Plugins_ and install the [Eclipse Code Formatter Plugin](https://plugins.jetbrains.com/plugin/6546-eclipse-code-formatter).

Restart you IDE, open the *Preferences* window again and navigate to _Other Settings_ -> _Eclipse Code Formatter_.

Select _Use the Eclipse Code Formatter_, then change the _Eclipse Java Formatter Config File_ to point to the
[src/main/resources/io/smallrye/coderules/eclipse-format.xml](src/main/resources/io/smallrye/coderules/eclipse-format.xml) file in the [src/main/resources/io/smallrye/coderules](src/main/resources/io/smallrye/coderules) directory. Make sure the _Optimize Imports_ box is ticked, and
select the [src/main/resources/io/smallrye/coderules/eclipse.importorder](src/main/resources/io/smallrye/coderules/eclipse.importorder) file as the import order config file.

## The small print
All SmallRye projects are open source projects, please act responsibly, be nice, polite and enjoy!

## Credits
Many thanks to the [quarkus](https://github.com/quarkusio/quarkus/) project where we "borrowed" most of the text for this page and used their Eclipse formatter as a starting point for the SmallRye formatter.

