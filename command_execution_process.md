Command Execution Process
from Your UNIX, the Ultimate Guide pg.252

1. Parses the command into words (white space signals the end of word), puts 1 space between each.
2. Second pass variables are replaced with their values (if syntax is correct)
3. Commands in ` ` or $( ) are executed (this is recursive – steps 1-3 might need to be repeated) and their output strings are substituted into the command.
4. The shell checks to see if any files (stdin, stdout, stderr) are redirected, if so the redirected files are opened.
5. Wildcards are expanded and replaced with matching filenames.
6. The shell looks for the directory containing the executable using the PATH variable.

echo `ls f*` list of $myName
