[code](code.md)

## Ruby
(41% through Codecademy course)

### Arithmetic operators
- `+`  Addition
- `-`  Subtraction
- `*`  Multiplication
- `/`  Division
- `**` Exponentiation (2 to the power of 3 or 2 x 2 x 2 = 8)
- `%`  Modulo (Remainder)

### Comparators / Relational Operators
- `==` equal to
- `!=` not equal to
- `<=` less than or equal to
- `>=` greater than or equal to
- `<` less than
- `>` greater than

### Boolean Operators / Logical Operators
- `&&`:  'and'  results in true when both expression on either side of `&&` are true
- `||`:  'or'   (inclusive or) evaluates to true when one or the other or both expressions are true
- `!`: 'not'  makes true values false, and vice-versa

### Assignment Operators
- `=`
- `+=` increment by "value"
- `-=` decrease by "value"
- `*=` multiply by "value"
- `/=` divide by "value"

### Arrays

- Square brackets: `[]`
- Can be booleans, strings, integers etc.
- Indexed from 0
```ruby
array = [5, 7, 9, 2, 0]
array[2]
```
 - returns "9", since "9" is at index 2

```ruby
string_array = ["yes", "no", "top", "pot", "fool"]
```

### Multidimensional Arrays

```ruby
multi_d_array = [[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0]]

multi_d_array.each { |x| puts "#{x}\n" }
```
`\n` means newline (escape sequence)

#### Two Dimensional Array
```ruby
my_2d_array = [["poop", "woop", "doop"], ["goop", "boop", "soup"]]
```

### Hashes
- A hash is a collection of key-value pairs
- Values are assigned to keys using =>


#### Creating a Hash
- `hash_name = Hash.new(0)` creates a new hash with name "hash_name" and default value "0".
- Hash must be capitalized. Without (0), hash will be empty.

or literal notation:

```ruby
hash_name = {
  "name" => "Jess",
  "age" => "34",
  "height" => "167"
  }
```

#### Adding to a Hash
With literal notation just add a new key-value pair directly between the curly braces (as in above section). If we used Hash.new, we can add to the hash using bracket notation:

```ruby
pets = Hash.new
pets["Stevie"] = "cat"
```

#### Accessing Hash values
```ruby
print hash_name["name"]
```

---

See also [JavaScript](javascript/notes.md)
