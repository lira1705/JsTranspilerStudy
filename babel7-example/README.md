# Updating to Babel 7

## What needs to be updated 

1. Use babel.config.js to centralize configurations of your packages;

3. All of those packages below are deprecated and it's necessary to change the 'preset' for 'preset-env';
  * babel-preset-es2015
  * babel-preset-es2016
  * babel-preset-es2017
  * babel-preset-latest

3. Remove @babel/polyfill and substitute it with core-js;  

5. Remove the 'preset-' and 'plugin-' from the pakages in .babelrc;

6. Change all babel packages names in package.json and babel config files;
 * babel-core -> @babel/core
 * babel-cli -> @babel/cli
 * env -> "@babel/env"

6. Switch the transform for the proposal in plugins that aren't yearly releases;
 * @babel/plugin-transform-function-bind -> @babel/plugin-proposal-function-bind

7. Remove the year from packages;  
 * @babel/plugin-transform-es2015-classes -> @babel/plugin-transform-classes  

8. Turn the presets in a list;  
 * "presets": "@babel/preset-env, @babel/preset-react" -> "presets": ["@babel/preset-env", "@babel/preset-react"]  

9. Scripts should be aware that the path should be relative to the babel config file;

11. Add @babel/runtime-corejs2 if @babel/runtime was used;

12. Change the transform-runtime for the @babel/plugin-transform-runtime;  

13. Update @babel/plugin-transform-export-extensions to @babel/plugin-proposal-export-default-from and @babel/plugin-proposal-export-namespace-from;

### For each topic and more informations consult the official docs: https://babeljs.io/docs/en/v7-migration
