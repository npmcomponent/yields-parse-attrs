*This repository is a mirror of the [component](http://component.io) module [yields/parse-attrs](http://github.com/yields/parse-attrs). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/yields-parse-attrs`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# parse-attrs

  attributes parser.

## Installation

    $ component install yields/parse-attrs

## Example

```js
assert('baz' == parse('foo="baz"').foo);
assert('baz' == parse("foo='baz'").foo);
assert('baz' == parse('foo=baz').foo);
assert('' == parse('foo').foo);
var attrs = parse('foo bar baz');
assert('' == attrs.foo);
assert('' == attrs.bar);
assert('' == attrs.baz);
var attrs = parse('foo=bar baz="foo bar" bar=\'baz\'');
assert('bar' == attrs.foo);
assert('baz' == attrs.bar);
assert('foo bar' == attrs.baz);
```

   

## License

  MIT
