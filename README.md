= ezparse =

A commandline utility to parse text files with ease

== Syntax ==

Get all words from a file and print them seperated by commans:

    ezparse --all --matching "\w" --join ", " example.txt

Get the first matching IP Addreess from `ifconfig -a` output:

    ezparse --first --matching "^(([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])\.){3}([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])$"

Print all files starting with `.` (hidden files):

    ezparse --all --matching "\s\.(.+)" --group 1 --join ", "
