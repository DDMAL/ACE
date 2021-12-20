# ACE 2.2.2
by Cory McKay (ACE 1.x and 2.x) and Jessica Thompson (ACE 2.x)
CIRMMT / Marianopolis College / McGill University
Copyright (C) 20212(GNU GPL)


### OVERVIEW

ACE is a metalearning classification framework that automatically experiments
with various dimensionality reduction and machine learning techniques to find
an approach that is well suited to each particular application. ACE is designed
primarily with the needs of music classification in mind, but may be used for
arbitrary classification tasks. ACE can read the standardized ACE XML 1 formats
as well as University of Waikato Weka ARFF files.

ACE 2.x is a significant redesign and expansion and improvement of ACE 1.1, 
which is also available at http://jmir.sourceforge.net. It should be noted,
however, that the ACE 2.x GUI is not yet complete; it can currently only 
display ACE XML data, but may not perform machine learning operations on it. 
The command line interface is fully functional, however, and users may perform
the full range of machine learning operations with it (or via the API, if they
prefer).

ACE was developed as part of the jMIR music classification research software
suite, and may be used either as part of  this suite or independently.


### MANUAL

A folder entitled "ACE_Manual" is extracted upon installation. This holds 
HTML files that provide many more details than this README document. Open the
"ACEManual.html" file to access the manual.


### GETTING MORE INFORMATION

More information on jMIR is available at http://jmir.sourceforge.net.

Please contact Cory McKay (cory.mckay@mail.mcgill.ca) with any bug reports
or questions relating to the software. 


### LICENSING AND LIABILITY 

This program is free software; you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT 
ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You may obtain a copy of the GNU General Public License by writing to the Free
Software Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.

This project software makes use of two included third-party products.

The University of Waikato Weka data mining package is used to parse and
save Weka ARFF files. This software is also available under the GNU GPL,
and more information on it is available at 
http://www.cs.waikato.ac.nz/ml/weka. 

This project also includes software developed by the Apache Software 
Foundation (http://www.apache.org), namely the Xerces library, which is used
to parse XML files. The Xerces license can be accessed via the manual.


### COMPATIBILITY

This software is written in Java, which means that it can theoretically be run
on any system that has the Java Runtime Environment (JRE) installed on it. It 
is recommended that this software be used with Windows, however, as it was 
developed and tested under the Windows operating system, and the interface's 
appearance was developed under Windows. Although the software should 
theoretically run under OS X, Linux, Solaris or any other operating system with
the JRE installed on it, users should be advised that the software has not yet 
been fully tested on other platforms, so difficulties may be encountered.

The current version of ACE was developed and tested with version 17 of the
JDK (Java Development Kit), and because it uses certain features not necessarily
present in earlier versions of Java, it is suggested that users have Java 17 or
later installed on their systems in order to run jSymbolic properly.


### INSTALLING THE JAVA RUNTIME ENVIRONMENT

If your system already has the JRE installed, as will most typically be the
case, you may skip this section. If not, you will need to install the JRE in
order to run this project. The JRE can be downloaded for free from the Java web
site. The JDK typically includes the JRE, or the JRE can simply be installed
alone.

When the JRE download is complete, follow the installation instructions that
come with it in order to install it.


### INSTALLING THE PROJECT

The project can be accessed at http://jmir.sourceforge.net. This distribution
includes a pre-compiled Jar file, the source code and extensive documentation. 
All of this is delivered in a zipped file, from which the project files can be
extracted.

There are two versions of the project, namely the developer version and the
user version. The user version contains everything needed to run the project,
but does not include any source code. The developer version does include
source code, presented in the form of a NetBeans project.

The user version unzips into a single directory. Installation simply involves 
copying this directory into any desired location.

The following directories are contained in the developer zip file:

- ACE: The ACE project, presented in the form of a NetBeans project. Contains the
following directories and files:
	- ACE_Manual: Contains the project's HTML manual.
	- dist: Contains a pre-compiled ACE.jar file (and associated
	libraries) for direct inclusion in other projects.
	- javadoc: Javadoc documentation for the project source code.
	- licenses: Licenses associated with the project and its dependencies.
	- nbproject: NetBeans project files. This is only relevant to those
	wishing to use the software in a NetBeans IDE context; it is certainly
	possible to use the software in other development environments as well.
	- src: The project's source code.
	- build.xml: NetBeans build instructions. Only relevant if using the
	NetBeans IDE.
	- manifest.mf: The manifest used when building the project Jar file.
	- README.txt: Basic overall documentation of the project.
- Third-Party-Jars: Contains the distributable third-party software used by 
the project. Also includes the jar files for other jMIR projects that this
project has as adependencies, if any. These need to be included in the project's
build (in the NetBeans context, this means adding the jar files found here as 
libraries).


### RUNNING THE SOFTWARE

A file named "ACE.jar" is produced upon installation. Double clicking
on this file will open the GUI. However, the GUI currently only allows
users to view and edit ACE XML 1.1 files, not to perform machine learning
tasks.

Users must use the command line to access the full range of ACE's
functionality. In Windows, for example, access DOS under by going
to the Start Menu, selecting Run and typing "cmd". Then use the "cd" 
command to move to the directory that contains the ACE.jar file. In
that directory, type:

	java -jar ACE.jar ...

The ... indicates the appropriate flags for the task that the user
wishes to perform. Details are provided in the ACE manual.

It should be noted that the JRE does not always allocate sufficient
memory for ACE to process large amounts of data. Running 
ACE using either of the above two methods could therefore result
in an out of memory error (although this is relatively rare).

It is therefore sometimes preferable to manually allocate a greater
amount of memory to ACE before running it. 1000 MB should be more
than enough for most situations. This can be done by entering the 
following at the command prompt:

	java -mx1000M -jar ACE.jar ...


### UPDATES SINCE VERSION 1.0

ACE 2.2.2
- Updated the saveToARFF method in ace.datatypes.DataBoard to auto-
generate feature definitions if they are not explicitly present.
- Fixed a bug in the GUI manual display.
- Updated support libraries.
- Minor documentation updates.

ACE 2.2.1
- Fixed a bug related to parsing ACE XML files.
- Updated UtilityClasses support libraries.

ACE 2.2
- Minor bug fixes
- Includes updated support libraries (UtilityClasses and Weka 3.6.1).

ACE 2.0:
- Improved API: The overall architectural structure of ACE 2.0 has
been entirely redesigned in order to simplify and facilitate the use
of ACE as a library by external software.
- Improved Command Line Interface: The command line interface has been
improved in order to make its use more intuitive and in order to provide
users with additional ways of customizing processing.
- Updated GUI: A GUI is now available for viewing and editing ACE XML
files. Meta-learning functionality is still restricted to the command 
line interface and API at this point, however, although there are plans
to expand the GUI functionality.
- Improved Cross-Validation: ACE now performs its own customized
cross-validation in order to provide new options and more statistics 
than were available when Weka's cross-validation implementation that 
was previously used.
- ACE XML ZIP and Project Files: The ACE XML Project and ZIP files 
allows users to associate multiple ACE XML files together so that they
may be automatically saved or loaded together, and the ZIP format makes
it possible to package all files referred to in a Project file into a
single compressed ZIP file.
