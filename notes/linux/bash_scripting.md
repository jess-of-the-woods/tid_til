[linux terminal](terminal.md)

## BASH scripting

starts with a hashbang (`#!`) & reference to thing that runs the script e.g.
- `#! /bin/bash`: bash script
- `#! /usr/bin/env node`: node script

- [Beginners Bash Scripting](https://help.ubuntu.com/community/Beginners/BashScripting)

files should have the suffix '.sh' e.g. 'helloworld.sh'

run with `bash helloworld.sh`

`chmod +x helloworld.sh`: To make the file executable.

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

### If, Else
```sh
if [ <condition> ]; then {
  #this code will execute
}
else {
  #this code will execute
}
fi
```

### Else if
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
