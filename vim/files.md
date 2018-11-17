Working with files
==================

Open file at a certain line  `vim +100 filename`

Write changes to the file  `:w`

Write to _newfilename_   `:w newfilename`   
_Does not write changes to the current file_

Save as _newfilename_   `:sav newfilename`

Quit without saving  `:q!`

Write changes and quit  `:wq`

Forgot to open file with sudo?  `:w !sudo tee %`

Edit another file  `:e filename`     
_Use Tab for automatic file name completion_    
_Use `:pwd` and `:cd` to set the working directory_    
_To set the working directory to the one of the current file `:cd %:p:h`_

When you edit a new file, it will be loaded into a new buffer.


Buffers
-------

_A buffer is a file loaded into memory for editing. The original file remains unchanged until you write the buffer to the file._

List buffers  `:ls`

Edit a buffer by number or file name `:b3`  `:b filename`

Edit first / prev / next / last buffer  `:bf` `:bp` `:bn` `:bl`

Delete current buffer  `:bd`


Windows
-------

_A window is a viewport on a buffer._

Open a new empty widow (horizontally / vertically)   `:new` `:vnew`

Open a file in a new window (split horizontally / vertically)  `split: filename` `vsplit: filename`    
_(or just `sp` and `vsp`)_

Exchange current window with next one  `Ctrl+w x`

Move to the window on the left / down / up / right side  `Ctrl+w h` `Ctrl+w j` `Ctrl+w k` `Ctrl+w l`

Move to the previously chosen window   `Ctrl+w p`

Close all other windows   `:only` or `Ctrl+w o`

Close current window    `:q` or `Ctrl+w c`

Move _the window_ to the left / down / up / right   `Ctrl+w H` `Ctrl+w J` `Ctrl+w K` `Ctrl+w L`


Tabs
----

_A tab page holds one or more windows. Closing the last window of a tab closes the tab too._

Open a new tab with an empty window / edit a file in a new tab    `:tabe`  `:tabe filename`

Close current tab page   `:tabc`  `tabc!`

Close all other tab pages   `:tabo`  `:tabo!`

Go to the next tab / tab number 4    `:tabn` `:tabn 4`







