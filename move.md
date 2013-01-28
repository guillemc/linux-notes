Moving inside files
===================

Move left / down / up / right  `h` `j` `k` `l`


Paging
------

Move to the top of the file  `gg`

Move to the bottom of the file  `G`

Go to line 30 of the file  `30G`

Page forward / backward  `Ctrl+f` `Ctrl+b`

Up / down a half-page  `Ctrl+u` `Ctrl+d`

Place cursor on the highest/middle/lowest line of the screen:  `H` `M` `L`


Line
----

Move to the beginning / end of line  `0` `$`

Move (forward) to the beginning / end of the next word  `w` `e`    
*(use `W` and `E` to treat word as a whitespace-separated sequence of chars)*

Move (backwards) to the beginning / end of previous word  `b` `ge`   
*(use `B` and `gE` to treat words as a whitespace-separated sequence of chars)*

Move (forward)  just until / up to the next "(" char in line  `t(` `f(`

Move (backwards) just until / up to the previous ")" char in line `T)` `F)`

Use `;` to repeat the last `f`, `t`, `F` or `T`


Searching, matching, jumping
----------------------------

Search forward / backwards for a pattern  `/searchterm` `?searchterm`

Search forward / backwards for the word under cursor  `*` `#`    
_(you can use `g*` and `g#` to make a partial match search)_

Repeat latest search, in same / reverse direction  `n` `N`

Go to the matching "(", "{" or "[" character   `%`    
*(install plugin matchit.vim for `%` to match more things, such as html tags)*

Mark a line as "a", and eventually move to it  `ma` `'a`






