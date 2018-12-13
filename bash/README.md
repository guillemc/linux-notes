Bash
====
### Command Line Editing

Move to the start of the line: `Ctrl+A`

Move to the end of the line: `Ctrl+E`

Move forward one word: `Alt+F`

Move backward one word: `Alt+B`

Clear the screen: `Ctrl+L`   
_(same as running `clear`)_

Kill text from cursor to end of line: `Ctrl+K`

Kill text from cursor to start of line: `Ctrl+U`

Yank (pull) killed text and insert it: `Ctrl+Y`


### Quoting
Single quotes: suppress all expansions.

Double quotes: keeps treating $, \` and \\ as special characters

```
$ echo some text ~ *.txt $(echo foo) {1..5}
some text /home/me a.txt b.txt c.txt foo 1 2 3 4 5

$ echo "some text ~ *.txt $(echo foo) {1..5}"
some text ~ *.txt foo {1..5}

$ echo 'some text ~ *.txt $(echo foo) {1..5}'
some text ~ *.txt $(echo foo) {1..5}
```


### Redirections

Redirect standard error
```
./script.sh 2> errors.txt
```

Redirect both standard output and error
```
./script.sh > output.txt 2>&1
```

Suppress error messages
```
./script.sh 2> /dev/null
```
