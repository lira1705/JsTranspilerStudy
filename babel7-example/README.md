Updating to Babel 7

###Babel version 7 brings the babel.config.js to centralize configurations of all or only on package.

###All of those packages below are deprecated
babel-preset-es2015
babel-preset-es2016
babel-preset-es2017
babel-preset-latest

###Change the "preset" for "preset-env".

###Remove @babel/polyfill and substitute it with core-js  

###Remove the 'preset-' and 'plugin-' from the pakages in .babelrc

###Change all babel packages names in package.json and babel config files
Ex: babel-core -> @babel/core, babel-cli -> @babel/cli, env -> "@babel/env"

###Switch the transform for the proposal in plugins that aren't yearly releases
Ex: @babel/plugin-transform-function-bind -> @babel/plugin-proposal-function-bind

###Remove the year from packages  
Ex: @babel/plugin-transform-es2015-classes -> @babel/plugin-transform-classes  

###Turn the presets in a list  
Ex: "presets": "@babel/preset-env, @babel/preset-react" -> "presets": ["@babel/preset-env", "@babel/preset-react"]  

###Scripts should be aware that the path should be relative to the babel config file

###Add @babel/runtime-corejs2 if @babel/runtime was used

###Change the transform-runtime for the @babel/plugin-transform-runtime  

###Update @babel/plugin-transform-export-extensions to @babel/plugin-proposal-export-default-from and @babel/plugin-proposal-export-namespace-from

###For each topic consult the official docs: https://babeljs.io/docs/en/v7-migration
