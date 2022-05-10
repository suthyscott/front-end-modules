# JS Modules

This repo illustrates how to use js modules to import variables between vanilla js files. The config.js file is an example of how this technique can be used to keep sensitive data from being pushed to GitHub

In your html files, designate all js scripts as `type='module'`.

In your js files, export any desired variables using the `export` keyword. See config.js and index.js

In the js file where you would like to access the exported variable, use this syntax: `import {variablename} from 'filepathtoexportingfile'`. See page.js. Note that you MUST have the .js extension on the file path for the import statement. 

### Private variables

To use this pattern to keep sensitive data (like an api key) secret, store all such variables in a file such as config.js. Then add that file to your .gitignore to stop it being tracked by GitHub. 