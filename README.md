Simple Linear Regression
===
[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Dependencies][dependencies-image]][dependencies-url]

> Computes a least squares estimator of a [linear regression](http://en.wikipedia.org/wiki/Simple_linear_regression) model having a single explanatory variable.


## Installation

``` bash
$ npm install compute-linear-regression
```

For use in the browser, use [browserify](https://github.com/substack/node-browserify).


## Usage

``` javascript
var lr = require( 'compute-linear-regression' );
```

#### lr( x, y[, opts] )

Computes a least squares estimator of a [linear regression](http://en.wikipedia.org/wiki/Simple_linear_regression) model having a single explanatory variable.

``` javascript
var x, y, results;

// Independent (explanatory) variable array:
x = [ ];

// Dependent (response) variable array:
y = [ ];

results = lr( x, y );
// returns {...}
```

The basic returned `results` object is comprised as follows:

``` javascript
{
	'coefficients': {
		'intercept': Number,
		'slope': Number
	}
}
```

The function accepts the following `options`:

* 	__accessors__: `object` providing accessor `functions`.
	-	__x__: accessor `function` for accessing explanatory values.
	-	__y__: accessor `function` for accessing response values.
*	__slope__: known slope.
*	__intercept__: known *y*-intercept.
*	__residuals__: `boolean` indicating whether to return the differences between each observation `y_i` and the corresponding prediction `y^{hat}_i`.
*	__ci__: `boolean` indicating whether to return estimate confidence intervals.
*	__summary__: `boolean` indicating whether to return a statistical summary.
*	__predictor__: `boolean` indicating whether to return a predictor `function`.
*	...




## Examples

``` javascript
var lr = require( 'compute-linear-regression' );
```

To run the example code from the top-level application directory,

``` bash
$ node ./examples/index.js
```


## Tests

### Unit

Unit tests use the [Mocha](http://mochajs.org/) test framework with [Chai](http://chaijs.com) assertions. To run the tests, execute the following command in the top-level application directory:

``` bash
$ make test
```

All new feature development should have corresponding unit tests to validate correct functionality.


### Test Coverage

This repository uses [Istanbul](https://github.com/gotwarlost/istanbul) as its code coverage tool. To generate a test coverage report, execute the following command in the top-level application directory:

``` bash
$ make test-cov
```

Istanbul creates a `./reports/coverage` directory. To access an HTML version of the report,

``` bash
$ make view-cov
```


---
## License

[MIT license](http://opensource.org/licenses/MIT). 


## Copyright

Copyright &copy; 2015. Athan Reines.


[npm-image]: http://img.shields.io/npm/v/compute-linear-regression.svg
[npm-url]: https://npmjs.org/package/compute-linear-regression

[travis-image]: http://img.shields.io/travis/compute-io/linear-regression/master.svg
[travis-url]: https://travis-ci.org/compute-io/linear-regression

[coveralls-image]: https://img.shields.io/coveralls/compute-io/linear-regression/master.svg
[coveralls-url]: https://coveralls.io/r/compute-io/linear-regression?branch=master

[dependencies-image]: http://img.shields.io/david/compute-io/linear-regression.svg
[dependencies-url]: https://david-dm.org/compute-io/linear-regression

[dev-dependencies-image]: http://img.shields.io/david/dev/compute-io/linear-regression.svg
[dev-dependencies-url]: https://david-dm.org/dev/compute-io/linear-regression

[github-issues-image]: http://img.shields.io/github/issues/compute-io/linear-regression.svg
[github-issues-url]: https://github.com/compute-io/linear-regression/issues
