# webfly-cfg [![Build Status](https://secure.travis-ci.org/afroware/webfly-cfg.git?branch=master)](http://travis-ci.org/afroware/webfly-cfg)

> The Webfly config (`.webflyrc`) reader and writer.


## Install

```sh
$ npm install --save webfly-cfg
```


## Usage

#### .load()

Loads the webfly configuration from the configuration files.


#### .get(key) - NOT YET IMPLEMENTED

Returns a configuration value by `key`.   
Keys with dots are supported to access deep values.


#### .set(key, value) - NOT YET IMPLEMENTED

Sets a configuration value for `key`.   
Keys with dots are supported to set deep values.


#### .del(key) - NOT YET IMPLEMENTED

Removes configuration named `key`.   
Keys with dots are supported to delete deep keys.


#### .save(where, callback) - NOT YET IMPLEMENTED

Saves changes to `where`.   
The `where` argument can be a path to a configuration file or:

- `local` to save it in the configured current working directory (defaulting to `process.cwd`)
- `user` to save it in the configuration file located in the home directory


#### .toObject()

Returns a deep copy of the underlying configuration object.   
The returned configuration is normalised.   
The object keys will be camelCase.


#### #create(cwd)

Obtains a instance where `cwd` is the current working directory (defaults to `process.cwd`);

```js
var config = require('webfly-cfg').create();
// You can also specify a working directory
var config2 = require('webfly-cfg').create('./some/path');
```


#### #read(cwd)

Alias for:

```js
var configObject = (new Config(cwd)).load().toJson();
```


#### #normalise(config)

Returns a new normalised config object based on `config`.   
Object keys will be converted to camelCase.


## License

Released under the [MIT License](http://www.opensource.org/licenses/mit-license.php).
