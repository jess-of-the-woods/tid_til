[linux terminal](terminal.md)

## BASH scripting

- [basics](#basics)
- [comments](#comments)
- [variables](#variables)
  - [quoting](#quoting)
  - [command substitution](#command-substitution)
- [running scripts](#running-scripts)
  - [source](#source)
- [if statements](#if-statements)
  - [if else](#if else)
  - [else if](#else-if)
- [arithmetic relational operators](#arithmetic-relational-operators)
- [links](#links)

### basics
bash scripts start with a hashbang `#!` & reference to thing that runs the script e.g.
- `#!/bin/bash`: bash script or `#!/usr/bin/env bash`
- `#!/usr/bin/env node`: node script

files should have the suffix '.sh' e.g. 'helloworld.sh' although its not necessary

### comments
```bash
# This is a comment, it will not be executed.
```

### variables

```bash
#!/bin/bash
message='Hello World'
echo $message

exit $0
```
its a convention to put environment variables in all capitals, but regular variables (within a script) in lowercase.

no spaces around =. e.g. `message = "this is a string"` is wrong & won't work.

#### quoting
```bash
some_number=10
echo "this is my ${some_number}th beer"
```
will work whereas
```bash
some_number=10
echo "this is my $some_numberth beer"
```
will not work

#### command substitution
surround expressions in backticks: `

```bash
echo "there are `wc -l < /etc/group` lines in the /etc/group file"
```

### running scripts
`chmod +x helloworld.sh`: To make the file executable. (see also [chmod](terminal.md#chmod))

run with `bash helloworld.sh` or `./helloworld.sh`

#### source
the source command will run a script and also integrate (or make available) all the variables in script in current shell.

e.g. `source helloworld.sh` or `. helloworld.sh`

### arguments
- `$#`: number of args the script was run with
- `$0`: the filename of our script
- `$1..$n`: script arguments

e.g.
```bash
our_file_name=$0
echo $ourfilename
number_of_args=$#
echo "The first 3 arguments were ${1}, ${2} and ${3}"

```

### if statements
```bash
if [ <condition> ]; then {

}
fi
```

e.g.
```bash
#!/bin/bash
name="Margaret"
if [ $1 = $name ]; then
  echo "Hi $name"
fi

```

#### if, else
```sh
if [ <condition> ]; then {
  #this code will execute
}
else {
  #this code will execute
}
fi
```

#### else if
```sh
if [ <condition> ]; then {
  #this code will execute
}
elif [ <condition> ]; {
  #this code will execute
}
else {
  #this code will execute
}
fi
```

### arithmetic relational operators
- `-lt`: less than
- `-gt`: greater than
- `-le`: less than or equal
- `-ge`: greater than or equal
- `-eq`: equal
- `-ne`: not equal

e.g. `[ 1 -eq $SMALLNUMBER ]`


---

## Links
- [Beginners Bash Scripting](https://help.ubuntu.com/community/Beginners/BashScripting)
