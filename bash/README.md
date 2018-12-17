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


### History

In our `~/.bashrc` file, we make the following adjustments:

```
# save last n entries to disk
HISTFILESIZE=10000

# load last n lines into memory
HISTSIZE=5000

# when shell exits, append to history instead of overwrite
# (useful with multiple bash sessions, otherwise only the last one is saved)
shopt -s histappend
```

Then we `source ~/.bashrc` to make the changes effective.


We can search backwards in history with `Ctrl+R`, then typing part of the
command we want to search.

If we have already started typing something and want to search for it, we
can do:

```
Ctrl+ARYR
```

Explanation:

- `Ctrl+A` moves the cursor to the beginning of the line.
- `Ctrl+R` starts reverse search, and as a side effect puts the existing text in the clipboard.
- `Ctrl+Y` pastes the text.
- `Ctrl+R` performs the search of the pasted text.
