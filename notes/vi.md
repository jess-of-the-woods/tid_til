[terminal](linux/terminal.md) | [tools](tools.md)

## Vim/Vi
- `vi`: to open Vi/Vim
- `vi path/filename`: open (new/existing) file in Vim.

### modes
Vim has different modes, command mode, extended mode & input mode. 'esc' & 'i' alternate between command & input/insert modes.

`i` enters input/insert mode, `esc` to enter command mode, then `:` to enter extended mode.
### command mode
- `i`: insert mode
- `a`: append mode
- `R`: replace mode

  ### moving around
  - `j` & `k`: up & down
  - `h` & `l`: left & right
  - `g`: go to start of document
  - `G`: go to end of document
  - `3G`: go to 3rd line
  - `w`: move one word to the right
  - `b`: move one word to the left
  - `0`: go to start of line
  <!-- -  -->

  ### basics
  - `yy`: copy line
  - `yw`: copy word (`3yw`: copies 3 words)
  - `P`: paste above/before
  - `p`: paste below/after
  - `dd`: delete line
  - `cw`: replace word (enter insert mode), `dw` to delete word
  - `D`: delete to end of line
  - `shift + x`: to uncomment??

## extended mode
- `:q` then enter to quit.
- `:wq` or `:x` to write to file & quit
- `:q!` to discard changes.
- `:r existingFile.txt`: read in existing file (can use tab-completion)
- `r!date`: read in output of a command (e.g. date command)

<!-- ---

See also -->
