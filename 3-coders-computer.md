Read 02: The Coder's Computer

# Text Editors
[Choosing a Text Editor](https://medium.com/@theoldercoder/choosing-a-text-editor-3e56f71bd636) Learnings
* a very personal choice
* they are all pretty similar
* the one your enjoy using the most
* it's important for software developers to be thoughtful about their selection of what they use to write code because a good-fit editor will facilitate the programming process - so you can accomplish more with minimal effort

## What is a test editor?
* It's software you downladn and install on your computer or access online through your web browser
* It allows you to write and manage text, esp that you write to build a site

## Important features to look for
* Accomplish more with minimal effort
* **code completion** - start typing and it displays possible suggestions based on what you've already typed - saves time; also
  * closing of tags, brackets, quotation marks
  * Emmet - shorthand language for HTML and CSS helps to write more efficiently
* **syntax highlighting** - colorizes text - attributes are different color than elements, which are different from copy - helps you look for errors more easily and makes text easier to read
* **theme varieties** to reduce eyestrain and fatigue - usually developer use a dark background and bright text - easier on the eyes
* healthy selection of available extensions - like plugins

## Software that comes with your computer
* Mac is *Text Edit*
* Windows *Notepad*
* Linux - each dist has its own text editor installed - go by different names like "Gedit"
* Don't usually have many of the features discussed above - they are bare bones
* Caveats if you use the one that comes with your computer:
  * create code in plain text, no formatting options seen
  * create a folder on your computer (e.g. desktop) to store the entire website - save the files in appropriate folders
  * make sure to use the appropriate extension for your files names - e.g. main HTML is "index.html"; CSS "style.css"

## 3rd Party Options
* **Notepad ++** - free, windows only, syntax highlighting and completion, word completion, function completion, zoom in and out, online community, chat room, searchable wiki page
* **Text Wrangler/BB Edit** - mac only, text wrangler retired in 2017; BB Edit for purchase
* **VS Code** - made by Microsoft for windows, mac, linux; has the Emmet shorthand for HTML and CSS already built in - has it all - syntax highlighting, themese, extensions and code completion
* **Atom** - free for windows, mac and linux - brought to you by GitHub - has syntax highlighting, themes, extensions, the works - recommended to check it out
* **Brackets** - free, for windows, mac and linux - from Adobe - supports HTML, CSS and JS, more through extensions - uses "live preview" function
* **Sublime Text** - premium softward for purchase; otherwise free; fast, responsive, extensible; syntax highlighting, code completion, themes, extensions

* most is free and have some if not all of the features desired as listed above
* All widely used in development today

## Text Editors vs IDEs
* Text editor - edits and manages text, manages files
* IDE - Integrated Development Environment - suite of software - text editor, file manager, compiler, debugger all in one
  * like MS Outlook - email, calendar, task manager, to-do list

# Terminal
## [The Command Line](https://ryanstutorials.net/linuxtutorial/commandline.php)
* think of it as adding to the GUI, not leaving it
* 3 terminals open: 1 for work, 1 to bring up ancillary data, 1 for viewing manual pages
* it's a text-based interface to the system using "prompts"
* commands
  * ls - list - usually the first thing you type
  * "-" - options listed before other arguments

### Opening a terminal
* Mac & Linux - under utilities; Windows - Putty (free)
### Shell, Bash
* Shell - within a terminal - part of the OS that defines how the terminal will behave and look after running or executing commands - most common one is called *bash* which stands for Bourne again shell

### Commands
* shortcut - commands are stored in a history - use up and down arrows to travers and reuse rahter than re-typing commands previously 

## [Basic Navigation](https://ryanstutorials.net/linuxtutorial/navigation.php)
* Commands
  * pwd - Print Working Directory - tell you what your current directory is
  * ls - list - tells you what's in the present directory - `ls [options] [location]` - square brackets optional - e.g. `ls` only; `ls -l` - long listing; `ls /etc` - list the directories contents not the current directory; `ls -l /etc` - ls with both a command line option and argument - long listing of the directory /etc

* Paths
  * Absolute - specify a location (file or directory) in relation to the root directory - always begin with a "/"
  * Relative - specifiy a location (file or directory) in relation to where we currently are in the system - do not begin with a "/"
  * Root directory - very top of the structure denoted with a single slash "/"
  * `~` - shortcut for home directory - e.g. `ls ~/Documents`
  * `.` - references current directory - e.g. `ls ./Documents`
  * `..` - references parent directory - can use several times to keep going up the hierarchy - e.g. `../../`

* Moving around
  * `cd [location]` - if run cd without any arguments alwasy takes you back to home directory
  * tab completion - when you start typing a path, you may hit the Tab key at any time to invoke an auto complete action

# [More about Files](https://ryanstutorials.net/linuxtutorial/aboutfiles.php)
* everything is a file - text, directory, keyboard, monitor
* extensionless system - e.g. exe, txt, png etc - ignored
* command **file** can be used to find out what type of file it is - `file [path]`- path gets you to a location in the sytem and that is a file - tells you info on what type of file or directory it is
* case-sensitive
* spaces in names - use single or double quotes e.g. `cd 'Holiday Photos'` or use "escape characters" - e.g. `cd Holiday\ Photos` - removes the special meaning of the space - shortcut: use tab completion before encountering the space in the directory name and terminal will automatically escape any spaces in the name for you
* hidden files/directories - if begins with a "." then it is hidden - make hidden files this way too, remove it to make it unhidden
* `ls -a` will list contents of directory including hidden files - `ls` on its own will not