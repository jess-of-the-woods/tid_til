[notes](notes.md) | [to learn](toLearn.md)

## Testing

### Red, Green, Refactor
Write test, test should be non-passing.. i.e. 'red'. Write code, keep testing till test passes, i.e. green. Then refactor (improve code)

**Pattern**
- Arrange, Act, Assert

```javascript
testTools.equal($('span').text(), '5 April 2016')
```

pseudocode: when we render this template, we provide a date & the template renders that date in a span with class `datey.mcdateface`

- tap-spec
- Tape

TAP - test anything protocol

[Hihi TDD Gitbook](https://enspiral-academy.gitbooks.io/hihi-2016/content/weeks/1/monday.html)

See also [tools](tools.md)
