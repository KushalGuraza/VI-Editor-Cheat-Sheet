# VI-Editor-Cheat-Sheet

VI Editor Commands Reference Guide
1. Quitting VI
Command	Description
:x	Exit, saving changes
:q	Exit if no changes were made
ZZ	Save and exit if changes were made
:q!	Exit without saving
2. Inserting Text
Command	Description
i	Insert before cursor
I	Insert at the beginning of the line
a	Append after cursor
A	Append at the end of the line
o	Open a new line below
O	Open a new line above
r	Replace one character
R	Replace multiple characters
3. Motion (Navigation)
Command	Description
h	Move left
j	Move down
k	Move up
l	Move right
w	Move to the next word
W	Move to the next blank-separated word
b	Move to the beginning of the word
B	Move to the beginning of a blank-separated word
e	Move to the end of the word
E	Move to the end of a blank-separated word
( )	Move backward/forward by sentence
{ }	Move backward/forward by paragraph
0	Move to the beginning of the line
$	Move to the end of the line
1G	Move to the first line of the file
G	Move to the last line of the file
nG or :n	Move to the nth line of the file
fc	Move forward to character c
Fc	Move backward to character c
H	Move to the top of the screen
M	Move to the middle of the screen
L	Move to the bottom of the screen
%	Jump to matching (), {}, []
4. Deleting Text
Command	Description
x	Delete character under cursor
X	Delete character before cursor
D	Delete to the end of the line
dd or :d	Delete current line
dw	Delete a word
5. Copying & Pasting Text (Yanking)
Command	Description
yy or :y	Yank (copy) current line
y$	Yank until the end of the line
p	Paste after cursor or line
P	Paste before cursor or line
6. Changing Text
Command	Description
cw	Change word
C	Change to the end of the line
cc	Change the whole line
7. Working with Buffers
Named buffers allow saving and restoring text.

Command	Description
"a dw	Delete a word into buffer a
"a p	Paste from buffer a
8. Markers
Command	Description
mc	Set marker c on this line
`c`	Go to marker c (beginning of line)
'c	Go to the first non-blank character of marker c
9. Searching & Replacing
Command	Description
/pattern	Search forward for pattern
?pattern	Search backward for pattern
n	Repeat last search forward
N	Repeat last search backward
:s/pattern/string/flags	Replace pattern with string
g	Flag - Replace all occurrences
c	Flag - Confirm replacements
&	Repeat last :s command
10. Regular Expressions
Symbol	Description
.	Any single character (except newline)
*	Zero or more occurrences of any character
[abc]	Any single character from the set a, b, c
[^abc]	Any single character not in a, b, c
^	Start of line
$	End of line
\<	Beginning of a word
\>	End of a word
\( ... \)	Grouping
Regular Expression Examples
Pattern	Matches
/Hello/	Lines containing "Hello"
/^TEST$/	Lines containing only "TEST"
/^[a-zA-Z]/	Lines starting with a letter
/2134$/	Lines ending with "2134"
/\(21|35\)/	Lines containing "21" or "35"
11. Command Counts
Most commands can be preceded by a number:

Command	Action
5dw	Delete 5 words
3fe	Move to the 3rd occurrence of e
100i-<Esc>	Insert - 100 times
12. Ranges (For Multiple Lines)
Command	Description
:3,7d	Delete lines 3 to 7
:.,$s/pattern/string/g	Replace pattern from the current line to the end of file
:%s/old/new/g	Replace all occurrences of old with new
13. File Operations
Command	Description
:w file	Save to file
:r file	Read file into buffer
:e file	Edit file
!!program	Replace current line with output from program
14. Other Useful Commands
Command	Description
~	Toggle uppercase/lowercase
J	Join two lines
.	Repeat last command
u	Undo last change
U	Undo all changes on current line
Conclusion
This guide provides an easy reference for VI commands in Git Bash or any Unix-based terminal. Use it to navigate, edit, and efficiently manage text files using VI editor.

