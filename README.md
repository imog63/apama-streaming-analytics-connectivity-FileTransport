# apama-streaming-analytics-connectivity-FileTransport
Java based Connectivity Transport for reading/writing to files with [Apama](http://www.apamacommunity.com/).

## Description
File Transport Connectivity Plugin. Will operate on files line by line, either sending each line as a message towards the host or writing each message sent towards the transport. For more information on the Apama Connectivity Framework, as well as Apama in general, please see [the community website](http://www.apamacommunity.com/).

## Set-up
First, ensure you have an install of the Apama engine; a free edition is available at [the community website](http://www.apamacommunity.com/). This plugin assumes the user has familiarity with the basic structure of the install, more information of which can also be found on the community site.

Running and building of the sample requires access to the Correlator and Apama command line tools. To ensure that the environment is configured correctly for Apama, all the commands below should be executed from an Apama Command Prompt, or from a shell or command prompt where the bin\apama_env script has been run (or sourced on Unix).

### To build
The File Transport is most easily built with the Apache ANT tool from the directory containing 'build.xml'.

> ant

But if you do not have access to ANT, it will need to be built manually:

For Linux:
> mkdir build_output
> javac -cp $APAMA_HOME/lib/connectivity-plugins-api.jar -d build_output src/com/softwareag/samples/FileTransport.java
> jar -cf build_output/file-transport-plugins.jar -C build_output .
> cp build_output/file-transport-plugins.jar $APAMA_WORK/lib/

For Windows:
> mkdir build_output
> javac -cp %APAMA_HOME%/lib/connectivity-plugins-api.jar -d build_output src/com/softwareag/samples/FileTransport.java
> jar -cf build_output\file-transport-plugins.jar -C build_output .
> copy build_output\file-transport-plugins.jar %APAMA_WORK%\lib\

A successful build will produce output files for the File Transport:

	build_output\file-transport-plugins.jar

These should have already been copied to APAMA_WORK/lib where the correlator will load them from.

# Authors
[Callum Attryde](mailto:Callum.Attryde@softwareag.com)

______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
_____________
Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.
