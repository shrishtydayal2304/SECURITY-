NANO Command Optional Reading Material
How to Use Nano, the Linux Command Line Text Editor


When working on the command line, quite often you will need to create or edit text files. Two of the most powerful and popular command-line editors are Vim and Emacs. Both of them have a steep learning curve that can be intimidating to new users. For those who need a simple editor, there is nano.

GNU nano is an easy to use command line text editor for Unix and Linux operating systems. It includes all the basic functionality you’d expect from a regular text editor, like syntax highlighting, multiple buffers, search and replace with regular expression support, spellchecking, UTF-8 encoding, and more.

In this guide, explain the basic usage of the nano editor, including how to create and open a file, edit a file, save a file, search and replace text, cut and paste text, and more.

Installing Nano
Nano text editor is pre-installed on macOS and most Linux distros. To check if it is installed on your system type:

nano --version
The output will look something like this:

GNU nano, version 2.9.3
(C) 1999-2011, 2013-2018 Free Software Foundation, Inc.
(C) 2014-2018 the contributors to nano
Email: nano@nano-editor.org	Web: https://nano-editor.org/
If you don’t have nano installed on your system, you can install it using the package manager of your distribution.

Install Nano on Ubuntu and Debian
sudo apt install nano
Install Nano on CentOS and Fedora
sudo yum install nano
Opening and Creating Files


To open an existing file or to create a new file, type nano followed by the file name:



nano filename

This opens a new editor window, and you can start editing the file.

At the bottom of the window, there is a list of the most basic command shortcuts to use with the nano editor.

All commands are prefixed with either ^ or M character. The caret symbol (^) represents the Ctrl key. For example, the ^J commands mean to press the Ctrl and J keys at the same time. The letter M represents the Alt key.

You can get a list of all commands by typing Ctrl+g.

To open a file you must have read permissions to the file.



If you want to open a file with the cursor on a specific line and character use the following syntax:

nano +line_number,character_number filename
If you omit the character_number the cursor will be positioned on the first character.

Editing Files
Unlike vi, nano is a modeless editor, which means that you can start typing and editing the text immediately after opening the file.

To move the cursor to a specific line and character number, use the Ctrl+_ command. The menu on the bottom of the screen will change. Enter the number(s) in the “Enter line number, column number:” field and hit Enter.



Searching and replacing


To search for a text, press Ctrl+w, type in the search term, and press Enter. The cursor will move to the first match. To move to the next match, press Alt+w.



If you want to search and replace, press Ctrl+\. Enter the search term and the text to be replaced with. The editor will move to the first match and ask you whether to replace it. After hitting Y or N it will move to the next match. Pressing A will replace all matches.

Copping, cutting, and pasting
To select text, move the cursor to the beginning of the text and press Alt+a. This will set a selection mark. Move the cursor to the end of the text you want to select using the arrow keys. The selected text will be highlighted. If you want to cancel the selection press Ctrl+6

Copy the selected text to the clipboard using the Alt+6 command. Ctrl+k will cut the selected text.

If you want to cut whole lines, simply move the cursor to the line and press Ctrl+k. You can cut multiple lines by hitting Ctrl+k several times.



To paste the text move the cursor to where you want to put the text and press Ctrl+u.

Saving and Exiting
To save the changes you’ve made to the file, press Ctrl+o. If the file doesn’t already exist, it will be created once you save it.

To exit nano press Ctrl+x. If there are unsaved changes, you’ll be asked whether you want to save the changes.

To save the file, you must have at write permissions to the file. If you are creating a new file , you need to have write permission to the directory where the file is created.

Customizing Nano (nanorc)
When nano is launched, it reads its configuration parameters from the system-wide configuration file /etc/nanorc and from the user-specific files ~/.config/nano/nanorc and ~/.nanorc if the files are present.



Options specified in the user files take precedence over the global options.

Visit the nanorc page for a complete list of all available option.

Syntax Highlighting
Nano ships with syntax highlighting rules for most popular file types. On most Linux systems, the syntax files are stored in the /usr/share/nano directory and included by default in the /etc/nanorc configuration file.

/etc/nanorc

include "/usr/share/nano/*.nanorc"
Copy

The easiest option to enable highlighting for a new file type is to copy the file containing the syntax highlighting rules to the /usr/share/nano directory.

Set Nano as the Default Text Editor
By default on most Linux systems, the default text editor for commands such as visudo and crontab is set to vi. To use nano as the default text editor, you need to change the VISUAL and EDITOR environment variables .



Bash users can export the variables in the ~/.bashrc file:

~/.bashrc

export VISUAL=nano
export EDITOR="$VISUAL"
Copy

Basic Nano Usage
Below are the most basic steps for getting started with nano:

On the command prompt, type nano followed by the filename.

Edit the file as required.

Use the Ctrl-x command to save and exit the text editor.
