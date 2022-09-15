# create-vanilla-project-cli
A CLI tool to create a vanilla html/css/js project

Creating a CLI tool without using NPM:
To create a javascript based CLI tool for linux we need to take 3 steps:
- shbang line: '#! /usr/bin/env node' in our script file.
  This tells the bash to run the env command and then find node and run it
- chmod +x <your-script>.js
  This converts the script file into an executable
- alias <command>=/path/.. <your-script>.js
  This maps the <command> to the executable file so that it can be invoked using the <command> from anywhere.

Creating a CLI using using NPM:
This involves the following:
- shbang line: '#! /usr/bin/env node' in our script file.
  This tells the bash to run the env command and then find node and run it
- a new entry in the package.json file:
  "bin: {
    "command": "<path to script file>"
  }
  In turn, NPM makes this file an executable AND also maps the command to the file.