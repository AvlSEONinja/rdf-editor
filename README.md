# OpenLink Structured Data Editor

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Introduction](#introduction)
- [License](#license)
- [Dependencies](#dependencies)
- [Quick Build Guide](#quick-build-guide)
- [Deployment](#deployment)
- [Contributions](#contributions)
- [See Also](#see-also)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Introduction
The OpenLink Structured Data Editor enables editing of **RDF** documents (in **TURTLE** notation) stored in a
variety of *HTTP* accessible documents.  Actual document access requires the target document is
served from a system that supports at least one of the following open standards:

  - *Linked Data Platform (LDP)*
  - *WebDAV*
  - *SPARQL 1.1 Update*
  - *SPARQL Graph Protocol*

## License
Copyright 2014-2020 [OpenLink Software](mailto:opensource@openlinksw.com)

This software is licensed under the GNU General Public License (see
[COPYING](http://github.com/openlink/rdf-editor/blob/develop/COPYING)).

**Note**: that the only valid version of the GPL license as far as this project is concerned is the
original GNU General Public License Version 2, dated June 1991.



## Dependencies

This package uses a number of third party tools including:

Package  | Version | From
-------- | ------- | -------------------------------------
autoconf | 2.57    | http://www.gnu.org/software/autoconf/
automake | 1.9     | http://www.gnu.org/software/automake/
make     | 3.79.1  | http://www.gnu.org/software/make/
python   | 2.7     | http://www.python.org/
npm      | 1.3.10  | http://nodejs.org/

The above version are the minimum recommended versions of these packages. Older version of these
packages can sometimes be used, but could cause build problems.

The autogen.sh and configure scripts check for the presence and right version of some of the
required components.

To check the version number of the tools installed on your system, use one of the following commands:

  * autoconf --version
  * automake --version
  * make --version
  * npm --version

A disclosure of all the third party libraries this in this project uses can be found in the
[CREDITS](http://github.com/openlink/rdf-editor/blob/develop/CREDITS) file.



## Quick Build Guide

If the npm tool has already been installed on your system, the following commands

Install the grunt command-line interface:
```
npm install -g grunt-cli
```

Install the bower command-line interface:
```
$npm install -g bower
```

Generate the configure script:
```
$ ./autogen.sh
```

Run the configure command:
```
$ ./configure
```

Build the package:
```
$ make
```

The project contains several README* files that show in more detail how to build the OpenLink Structured Data
Editor in various operating system environments.



## Deployment

The build system creates both a *rdf\_editor\_dav.vad* file that can be used with the
[OpenLink Virtuoso Universal Server](http://virtuoso.openlinksw.com) or
[OpenLink Virtuoso Open Source Edition](http://github.com/openlink/virtuoso-opensource)
projects and a *rdf\_editor\_pkg.tar.gz* and *rdf\_editor\_pkg.zip* file that can be used to build and
deploy the application on many http servers such as:

- Apache

  * **Download and install Apache (v2.x)**.

  * **Extract Structured Data Editor**:

	unzip rdf\_editor\_pkg.zip -d [PATH]

  * **Add new drectory (/rdf-edtor) with Structured Data Editor to the server configuration**:

  * **Start Apache Server**.

	[APACHE HOME]/bin/httpd

  * **Usage**:

	[Default Browser] localhost:[port]/rdf-editor/index.html

- IIS (Windows Only)

  * **Start IIS**.

  * **Extract Structured Data Editor**:

	unzip rdf\_editor\_pkg.zip -d [IIS Root Path]

  * **Usage**:

	[Default Browser] localhost:[port]/rdf-editor/index.html

- Tomcat

  * **Download and install Tomcat (v8.x)**.

  * **Start Tomcat**.

	[TOMCAT HOME]/bin/startup

  * **Extract Structured Data Editor**:

	unzip rdf\_editor\_pkg.zip -d [TOMCAT HOME]/webapps/Root

  * **Usage**:

	[Default Browser] localhost:[port]/rdf-editor/index.html

- Node.js http-server

  * **Download and install Node.js**.

  * **Download and install NPM manager**.

  * **Extract Structured Data Editor**:

	unzip rdf\_editor\_pkg.zip -d [Structured Data Editor Path]

	The http-server is a simple, zero-configuration command-line http server.

  * **Installation**:

	npm install http-server -g

	This will install http-server globally so that it may be run from the command line.

  * **Start HTTP Server**:

	http-server [Structured Data Editor Path]/rdf-editor [options]

  * **Usage**:

	[Default Browser] localhost:[port]/index.html


The project contains several README* files that show how to deploy the OpenLink Structured Data Editor in
various operating system environments.


## Contributions

OpenLink Software publishes the rdf-editor source tree to GitHub and encourages everyone who is
interested in tracking the project to make an account there.

Users who mainly just want to track the code can use the following command to get a copy of the
tree:
```
$ git clone git://github.com/openlink/rdf-editor.git
```

At this point you can create your own work branch based on any of the branches available, create
bugfixes and commit them to your own branch and then use the 'git format-patch' command to generate
the appropriate diffs to send to [OpenLink Software](mailto:opensource@openlinksw.com):
```
mailto:opensource@openlinksw.com
```

Bugs and enhancement requests can be reported using the
[Github Issues](http://github.com/openlink/rdf-editor/issues/) interface:
```
http://github.com/openlink/rdf-editor/issues/
```

Developers are encouraged to fork the project using GitHub, create
their own feature branches from the development branch to make
enhancements/bugfixes and then send pull requests using the excellent
GitHub interface for the OpenLink team to examine and incorporate
the fixes into the develop tree for an upcoming release.

Github has excellent [documentation](http://help.github.com/) on how to fork a project, send pull
requests, track the project etc. on:
```
    http://help.github.com/
```

## See Also

  - [OSDE website](http://osde.openlinksw.com/)
  - [Github project](https://github.com/openlink/rdf-editor/)
  - [Dockerhub repository](https://cloud.docker.com/repository/docker/openlink/osde/)
  - [OpenLink Website](https://www.openlinksw.com/)
