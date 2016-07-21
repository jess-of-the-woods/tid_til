[notes](notes.md) | [to learn](../toLearn.md)

## Testing

### Red, Green, Refactor
Write test, test should be non-passing.. i.e. 'red'. Write code, keep testing till test passes, i.e. green. Then refactor (improve code)

**Pattern**
- Arrange, Act, Assert

```javascript
testTools.equal($('span').text(), '5 April 2016')
```

pseudocode: when we render this template, we provide a date & the template renders that date in a span with class `datey.mcdateface`

### Unit Testing
A software development process in which the smallest testable parts of an application, called units, are individually and independently scrutinized for proper operation. Unit testing is often automated but it can also be done manually. This testing mode is a component of Extreme Programming (XP), a pragmatic method of software development that takes a meticulous approach to building a product by means of continual testing and revision.

#### Testing with Tape
Test file should import into it whatever is being tested. See line 2.

test.js:
```javascript
var test = require('tape').test;
var add = require('./add');

test('The add method', function(t){
  var actual = add(1,2);
  var expected = 3;
  t.equal(actual, expected, 'should add two numbers correctly.');
  t.end();
});
```
run in terminal with `node test.js` or name of test file.

You can pipe the output to 'tap-spec' to prettify the output by running `node test.js | tap-spec` or define it as a script in package.json

You can also pipe output to 'tap-simple' which will only display failing tests. Use with nodemon

`"tdd": "nodemon -x\"./bin/tape/test/**/*.test.js | bin/tap-simple \""`

the above script assumes you have created a symlink to node_modules

#### Modules
- tap-spec
- tape
- 'TAP': Test Anything Protocol
- tap-simple

### Integration testing
(sometimes called integration and testing, abbreviated I&T) is the phase in software testing in which individual software modules are combined and tested as a group. It occurs after unit testing and before validation testing. Integration testing takes as its input modules that have been unit tested, groups them in larger aggregates, applies tests defined in an integration test plan to those aggregates, and delivers as its output the integrated system ready for system testing.[1]

---

## Links
- [Hihi Gitbook - Test Driven Development ](https://enspiral-academy.gitbooks.io/hihi-2016/content/weeks/1/monday.html)
- [JS Kata - Objects & Arrays](https://github.com/hihi-2016/js-kata-objects-and-arrays) - (EDA Repo)
- [Unit testing: How to get your team started - FunFunFunction #2](https://www.youtube.com/watch?v=TWBDa5dqrl8) - YouTube (up to 12:54)
- [JavaScript Tutorial: Unit Testing with Tape pt2](https://www.youtube.com/watch?v=JK3EvAV4QKU) - YouTube

See also [tools](tools.md)
