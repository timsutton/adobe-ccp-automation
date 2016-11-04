# Experimenting with automating CCP

Creative Cloud Packager has some basic support for having its builds be driven by an XML input file. This experiment takes a list of tuples of SAP Code and "base version", looks up the latest HD installer for that base version and creates a manifest XML to run a CCP Named Package build.

For example, After Effects CC 2015.3, released in June 2016, has a base version of 13.8.0. There was later an update, version 13.8.1, which can be built as a single installer package. This script would find that the most recent version of the CC 2015.3 "series" of After Effects is 13.8.1, and download and package that. The package will contain _no_ other optional updates for that item, such as Camera Raw.
