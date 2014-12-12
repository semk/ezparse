ezparse
=======

A commandline utility to parse text files with ease

Syntax
======

Get all words from a file and print them separated by commas:

    ezparse --all --matching "\w" --join ", " example.txt

Get the first 2 matching IP Addreess from `ifconfig -a` output:

    ifconfig -a | ezparse --first --matching "inet (\S+)" --group 1 --slice 3

Print all files starting with `.` (hidden files):

    ls -al | ezparse --all --matching "\s\.(.+)" --group 1 --join ", "
