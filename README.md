ezparse
=======

A commandline utility to parse text files with ease

Syntax
======

    usage: ezparse [options] [input_file]

        options:
            --all           Prints all the matches from the input.
            --first         Prints only the first match from the input.
            --last          Prints only the last match from the input.
            --slice         Prints only the matches as specified in this argument.
            --matching      The regular expression to match.
            --group         Use the group specified in this option while printing.
            --join          Specifies the delimiter while printing matches.

Examples
========

Get all words from a file and print them separated by commas:

    ezparse --all --matching "\w" --join ", " example.txt

Get the first 2 matching IP Addreess from `ifconfig -a` output:

    ifconfig -a | ezparse --first --matching "inet (\S+)" --group 1 --slice 3

Print all files starting with `.` (hidden files):

    ls -al | ezparse --all --matching "\s\.(.+)" --group 1 --join ", "
