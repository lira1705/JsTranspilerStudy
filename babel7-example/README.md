# Updating to Babel 7

## What needs to be updated 

### Change Package/Plugins/Presets for updated versions

1. It's necessary to change the 'preset' for 'preset-env' on the packages below;
* babel-preset-es2015
* babel-preset-es2016
* babel-preset-es2017
* babel-preset-latest
2. Remove the 'preset-' and 'plugin-' from the pakages in .babelrc;
3. Switch the transform for the proposal in plugins that aren't yearly releases;
  * @babel/plugin-transform-function-bind -> @babel/plugin-proposal-function-bind
4. Change all babel packages names in package.json and babel config files;
* babel-core -> @babel/core
* babel-cli -> @babel/cli
* env -> "@babel/env"
5. Remove the year from packages;  
* @babel/plugin-transform-es2015-classes -> @babel/plugin-transform-classes  
6. Change the transform-runtime for the @babel/plugin-transform-runtime;  

### Add/remove packages

1. Remove @babel/polyfill and substitute it with core-js;  
2. Add @babel/runtime-corejs2 if @babel/runtime was used;
3. Remove @babel/plugin-transform-export-extensions and add @babel/plugin-proposal-export-default-from and @babel/plugin-proposal-export-namespace-from;

### More adjustments
1. Use babel.config.js to centralize configurations of your packages;
2. Turn the presets in a list;  
* "presets": "@babel/preset-env, @babel/preset-react" -> "presets": ["@babel/preset-env", "@babel/preset-react"]  
4. Scripts should be aware that the path should be relative to the babel config file;

#### For each topic and more informations consult the official docs: https://babeljs.io/docs/en/v7-migration
