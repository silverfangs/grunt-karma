# grunt-karma-serial
This is a fork from the original [project](https://github.com/karma-runner/grunt-karma). The reason this is created is to solve the merging issue of [#108](https://github.com/karma-runner/grunt-karma/pull/108), which enables developers to run `grunt-karma` to test multiple files serially without the halt of the program execution when one of the test case has been failed. The original solution is provided by [gantaa](https://github.com/gantaa).


> Grunt plugin for [Karma](https://github.com/karma-runner/karma)

This current version uses `karma@0.13.x`. For using older versions see the
old releases of grunt-karma.

## Documentation
To use this package, please refer to the original [documentation](https://github.com/karma-runner/grunt-karma/blob/master/README.md).

## Getting Started
To install this package, you can install it via NPM:

```bash
$ npm install grunt-karma-serial
```

## Exit on Failure Option
You can add `exitOnFailure` option in your `karma`:

### Here's an example that puts the config in the Gruntfile:

```js
karma: {
  unit: {
    exitOnFailure: false,
    configFile: 'karma.conf.js',
    port: 9999,
    singleRun: true,
    browsers: ['PhantomJS'],
    logLevel: 'ERROR'
  }
}
```

The 'exitOnFailure' config property when false, will continue executing grunt tasks instead of having karma exit the process (warning: when set to false and running with multiple grunt tasks, the build will not be considered a 'failure' even if some tests failed).  The default value is true.  A value of true will exit the process on test failures and halt any further grunt executions.


## License
MIT License
