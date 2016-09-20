[terminal](terminal.md)

## Searching
- [find](#find)
- [locate](#locate)
- [grep](#grep)
- [sed](#sed)

### find
Syntax: `find ~/Downloads theFileImLookingFor`: Finds files/directories.
- `find -iname "markdown.*"`: search for files called markdown (`-iname`: case-insensitive)
- `find /home -iname "markdown.*"`: search for files in /home called markdown
- use `-type` & a letter, such as `f`: files, `d` directories, `l`: symbolic links etc. e.g. `find / -type d -iname "filename"`
- `find / -name "*song*" -user margaret -exec ls -l {} \;`: find files with the word 'song' somewhere in the name (case-sensitive), owned by user 'margaret', then execute 'ls -l' with the results.

hint: pipe results to less

### locate
based on an index of filesystem which is updated once a day. therefore can be out of date. some directories such as /tmp are excluded based on  `/etc/updatedb.conf`: config file for locate
- `locate "*.mp3"`
- `sudo updatedb`: to update 'locate' database/index

### grep
- 'G'lobal 'Re'gular expression 'P'rint (regex), used to look for line that matches a pattern inside files
- `grep "foo" words.txt` or `grep -i "foo" words.txt` or `grep -R searchterm /home/user/`
- `-i`: case-insensitive
- `-R`: recursive
- `-v`: invert
- `-n`: line number
- `^`: start of line
- `$`: end of line
- `..cept` finds `accept`, `except`

### sed
'stream editor', accepts standard input and modifies it based on an expression, before displaying it as output, for filtering & transforming text
