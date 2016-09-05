[linux terminal](terminal.md)

## BASH scripting

starts with a hashbang (`#!`) & reference to thing that runs the script e.g.
- `#! /bin/bash`: bash script
- `#! /usr/bin/env node`: node script


files should have the suffix '.sh' e.g. 'helloworld.sh'

run with `bash helloworld.sh`

`chmod +x helloworld.sh`: To make the file executable.

then run the script with `./scriptName.sh`

### Comments
```sh
# This is a comment, it will not be executed.
```

### Variables

```sh
#!/bin/bash
MESSAGE='Hello World'
echo $MESSAGE
```

### If statements
```sh
if [ <condition> ]; then {

}
fi
```

#### If, Else
```sh
if [ <condition> ]; then {
  #this code will execute
}
else {
  #this code will execute
}
fi
```

#### Else if
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

### Arithmetic relational operators
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
