Working with files
==================

Open file at a certain line  `vim +100 filename`

Write changes to the file  `:w`

Quit without saving  `:q!`

Write changes and quit  `:wq`

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

Open a file in a new window (split horizontally / vertically)  `split: filename` `vsplit: filename`    
_(or just `sp` and `vsp`)_

Exchange current window with next one  `Ctrl+w x`

Move to the window on the left / down / up / right side  `Ctrl+w h` `Ctrl+w j` `Ctrl+w k` `Ctrl+w l`

Move to the previously chosen window   `Ctrl+w p`

Close all other windows   `:only` or `Ctrl+w o`

Close current window    `:q` or `Ctrl+w c`

Move _the window_ to the left / down / up / right   `Ctrl+w H` `Ctrl+w J` `Ctrl+w K` `Ctrl+w L`



