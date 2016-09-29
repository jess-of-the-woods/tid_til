[terminal](linux/terminal.md) | [tools](tools.md)

## Vim/Vi
- `vi`: to open Vi/Vim
- `vi path/filename`: open (new/existing) file in Vim.

### modes
Vim has different modes, command mode, extended mode & input mode. 'esc' & 'i' alternate between command & input/insert modes.

`i` enters input mode, `esc` to enter command mode, then `:` to enter extended mode.
### command mode
- `i` = insert mode
- `a` = append mode
- `R` = replace mode

  ### moving around
  - `j` & `k` = up & down
  - `h` & `l`  = left & right
  - `g` = go to start of document
  - `G` = go to end of document
  - `3G` = go to 3rd line
  - `w` = move one word to the right
  - `b` = move one word to the left

  ### basics
  - `y` = copy line
  - `P` = paste here
  - `p` = paste after
  - `dd` = delete line
  - `w`: to move to next word, `cw` to replace word??
  - `shift + x`: to uncomment??

## extended mode
- `:q` then enter to quit.
- `:wq` or `:x` to write to file & quit
- `:q!` to discard changes.

<!-- ---

See also -->
