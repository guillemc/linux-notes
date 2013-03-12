Editing
=======

Enter insert mode
-----------------

_All these commands will put vim in insert mode. Press `Esc` to go back to command mode._ 

Insert at current cursor position   `i`

Insert at the beginning of the line  `I`

Append at current cursor position  `a`

Append at the end of the line   `A`

Insert new line below / above current line   `o` `O`

Change with a motion (to the end of the word, line...)  `cw` `c$`   
_(deletes up to the motion and leaves you in insert mode. `:set cpoptions+=$` to get visual hints)_


Replace mode
------------

Start replacing at the cursor position  `R`. Press `Esc` to go back to normal mode.


Deleting
--------

Delete char under / before the cursor  `x` `X`

Replace char under cursor  `r` 

Delete current line  `dd`

Delete to the end of the word (and following space)  `dw`

Delete just to the end of the word  `de`


Repeat, undo
------------

Repeat last change  `.`

Undo    `u`

Redo   `Ctrl+r`


Copy and paste
--------------

Copy (yank) a line  `yy` or `Y`

Yank a word (with or without space after word)   `yw` `ye`

Paste after / before cursor  `p` `p`     
_(If you yanked a line, it will place in a line below / above the current line)_    
_(Cut and paste works the same, but using `d` instead of `y`)_

Copy and paste using a specific copy buffer "a"  `"aY` `"ap`   
_(Use * to refer to the system clipboard)_


Visual mode
-----------

Enter character based / line based / block based visual mode  `v` `V` `Ctrl+v`    
_(then use movement commands to select chars / lines / columns)_

Reselect last selection made  `gv`


Search and replace
------------------

On current line  `:s/foo/bar/g`    
_(g stands for global and means all occurrences, not only the first one)_

On the whole file  `:%s/foo/bar/gc`    
_(use the c argument to ask for confirmation, i to force ignorecase, I to force noignorecase)_

Between marks "a" and "b"  `:'a,'bs/foo/bar/gc`

Inside a visual selection  `:'<,'>s/foo/bar/gc`

Regexps: see [vimregex.com](http://vimregex.com). Some quantifiers need escaping, such as `\+`, `\{n,m}`, but not `*`. Grouping needs escaping: `\([a-z]\+\)`.   

Example: in a php file containing an associative array 'key1' => 'val1', 'key2' => 'val2', etc. replace all values by their keys:

`%s/'\([^']\+\)' => '\([^']\+\)'/'\1' => '\1'/g`


