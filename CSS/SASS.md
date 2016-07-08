[CSS](CSS.md)

## Syntactically Awesome Style Sheets - SASS

### Variables

```css
$standard-border: 4px solid black`

.banner {
  border: $standard-border;
  }
```

Variables can use different data types. E.g. color, numbers, strings, booleans, null, lists, maps. Above variable is an example of a list.

**Map**

`(key1: value1, key2: value2)`


### &
In Sass, the & character is used to specify exactly where a parent selector should be inserted. It also helps write pseudo classes in a much less repetitive way.

For example, the following Sass:

```css
.notecard{
  &:hover{
      @include transform (rotatey(-180deg));  
    }
  }
```

will compile to the following CSS:

```css
.notecard:hover {
  transform: rotatey(-180deg);
}
```
