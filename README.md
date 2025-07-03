# TEXT-EDITOR-CONSOLE-BASED

class Textrunner;
class Line;
/*Line can have a MyString object or a char* only. You are not allowed to use std::string class implemented in stl.*/ 

Editors operates in multiple modes, each serving a distinct purpose:
Normal Mode: Used for navigation and text manipulation (default mode).
Insert Mode: Allows direct text entry and editing like notepad.
Command-Line Mode: Used to execute commands like save, quit, and search.

1. Normal Mode (Default Mode)
Description:
Activated automatically when the Editor starts.
Used for navigation, text manipulation, and executing commands.
Press i to enter Insert Mode.
Press : to enter Command Mode
Commands:
Navigation:
h: Move left
l: Move right
j: Move down
k: Move up
w: Move to the beginning of the next word
b: Move to the beginning of the previous word
0: Move to the beginning of the current line
$: Move to the end of the current line
gg: Move to the beginning of the file
G: Move to the end of the file
Ctrl+d: Scroll down half a page
Ctrl+u: Scroll up half a page
Deleting Text:
dd: Delete current line
D: Delete from cursor to the end of the line
x: Delete character under the cursor
Copying & Pasting:
yy: Yank (copy) current line
p: Paste copied content after current line
P: Paste copied content before current line
Undo & Redo:
u: Undo last action
Ctrl+r: Redo last undone action
Description:
Allows direct text insertion and editing.
Enter by pressing i in Normal Mode.
Exit by pressing Esc to return to Normal Mode.
Features:
Behaves like a notepad.
Commands:
Backspace: Delete character before cursor
Delete: Delete character after cursor
Ctrl-C: Copy selected text
Ctrl-V: Paste copied text
Shift + Arrow Keys: Select text
Enter: Insert a new line
Shift + Tab: Unindent (if indented)

3. Command-Line Mode (Executing Commands)
Description:
Activated by pressing : in Normal Mode.
Used for executing commands like save, quit, and search.
Exit by pressing Esc or Ctrl-C to return to Normal Mode.
Commands:
File Operations:
:w - Save file
:q - Quit Vim
:wq - Save and quit
:q! - Quit without saving
Find and Replace:
:/pattern - Search for pattern
:?pattern - Search backwards for pattern
:n - Move to next search occurrence
:N - Move to previous search occurrence
