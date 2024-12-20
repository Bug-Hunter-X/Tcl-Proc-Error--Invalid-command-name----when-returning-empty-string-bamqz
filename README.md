# Tcl Proc Error: Invalid command name "" when returning empty string

This repository demonstrates a common error in Tcl when a procedure attempts to return an empty string when a key is not found in a dictionary. The issue arises because Tcl interprets an empty string in a return statement as an attempt to execute a command with no name, leading to the "invalid command name "" error.

The `bug.tcl` file showcases the problematic code. The `bugSolution.tcl` file provides a corrected version.

## Bug
The `get_value` procedure attempts to handle missing keys by returning an empty string. However, Tcl misinterprets this as a command execution request, resulting in the error. 

## Solution
The solution involves explicitly returning an empty string using the `return` command with the empty string enclosed in quotes.