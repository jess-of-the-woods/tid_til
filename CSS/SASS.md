[CSS](CSS.md)

## SASS - Syntactically Awesome Style Sheets
([Guide](http://sass-lang.com/guide))

### Variables

```css
$standard-border: 4px solid black`

.banner {
  border: $standard-border;
  }
```

Variables can be different data types. E.g. color, numbers, strings, booleans, null, lists, maps. Above variable is an example of a list. They are declared with the `$`symbol and then the variable name.

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

### Mixins

a mixin lets you make groups of CSS declarations that you want to reuse throughout your site.

**Note**: Mixin names and all other Sass identifiers use hyphens and underscores interchangeably.

e.g.

```css
@mixin backface-visibility {
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  -moz-backface-visibility: hidden;
  -ms-backface-visibility: hidden;
  -o-backface-visibility: hidden;
}
```
