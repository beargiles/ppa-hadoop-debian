Hadoop packages
=

This directory contains the /debian files for the Hadoop packages.

Getting the Source
==

To get the overall Hadoop source use

```{bash}
$ git checkout git@github.com:apache/hadoop.git
```

To get a specific release, e.g., 2.9.0, cd into the hadoop directory
and use

```
$ git checkout rel/release-2.9.0
```

Building the Debian Package
==

To build an (unsigned) package cd into the hadoop directory, mkdir debian,
and copy the contents of the appropriate subdirectory into it. Update
the changelog. Update the 'control' file to specify the desired Ubuntu
release. (16.04 LTS is 'xenial', 18.04 LTS is 'bionic').

Once you're satified with the updated files build the Debian packages
with

```
$ dpkg-buildpackage -us -uc -nc
```
