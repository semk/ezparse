ezparse
=======

A commandline utility to parse text files with ease

Syntax
======

Get all words from a file and print them seperated by commans:

    ezparse --all --matching "\w" --join ", " example.txt

Get the first 2 matching IP Addreess from `ifconfig -a` output:

    ifconfig -a | ezparse --first --matching "inet (\S+)" --group 1 --slice 3

Print all files strong1arting with `.` (hidden files):

    ezparse --all --matching "\s\.(.+)" --group 1 --join ", " input.txt
