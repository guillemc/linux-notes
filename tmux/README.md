Tmux
====

By default the prefix is `Ctrl+B`.

Create new window: `prefix c`

Move between windows by number: `prefix 0-9`

Rename window: `prefix ,`

Kill window (when not responding, etc.): `prefix &`    
_Note that sometimes we accidentally might press `Ctrl+S` (which suspends the output in the bash shell).    
In that case we just need to press `Ctrl+Q` to resume output again._

Scroll: `prefix [`   
_Then use arrow keys to move up/down, `q` to quit._



### Splitting  windows into panes

Split window ( | ): `prefix %`

Split window ( - ): `prefix "`

Make panel fullscreen: `prefix z`
(and again to exit)

Move between panes: `prefix arrow_key`

Resize pane: `prefix Ctrl+arrow_key`
