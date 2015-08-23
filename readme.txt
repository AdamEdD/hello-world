
 LEARN YOU THE NODE.JS FOR MUCH WIN!
─────────────────────────────────────
 MY FIRST I/O!
 Exercise 3 of 13

Write a program that uses a single synchronous filesystem operation to read a file and print the number of newlines (\n) it contains to the console (stdout), similar to running cat file | wc -l.

The full path to the file to read will be provided as the first command-line argument. You do not need to make your own test file. 

-------------------------------------------------------------------------------

## HINTS

To perform a filesystem operation you are going to need the fs module from the Node core library. To load this kind of module, or any other "global" module, use the following incantation:

    var fs = require('fs')

Now you have the full fs module available in a variable named fs.

All synchronous (or blocking) filesystem methods in the fs module end with 'Sync'. To read a file, you'll need to use fs.readFileSync('/path/to/file'). This method will return a Buffer object containing the complete contents of the file.

Documentation on the fs module can be found by pointing your browser here:
  file:///usr/local/lib/node_modules/learnyounode/node_apidoc/fs.html

Buffer objects are Node's way of efficiently representing arbitrary arrays of data, whether it be ascii, binary or some other format. Buffer objects can be converted to strings by simply calling the toString() method on them. e.g. var str = buf.toString().

Documentation on Buffers can be found by pointing your browser here:
  file:///usr/local/lib/node_modules/learnyounode/node_apidoc/buffer.html

If you're looking for an easy way to count the number of newlines in a string, recall that a JavaScript String can be .split() into an array of substrings and that '\n' can be used as a delimiter. Note that the test file does not have a newline character ('\n') at the end of the last line, so using this method you'll end up with an array that has one more element than the number of newlines.

-------------------------------------------------------------------------------

 » To print these instructions again, run: learnyounode print
 » To execute your program in a test environment, run: learnyounode run program.js
 » To verify your program, run: learnyounode verify program.js
 » For help run: learnyounode help


Peters-iMac:~ peterdarcy$ gedit
-bash: gedit: command not found
Peters-iMac:~ peterdarcy$ geddit
-bash: geddit: command not found
Peters-iMac:~ peterdarcy$ clear


 LEARN YOU THE NODE.JS FOR MUCH WIN!
─────────────────────────────────────
 MY FIRST I/O!
 Exercise 3 of 13

Write a program that uses a single synchronous filesystem operation to read a file and print the number of newlines (\n) it contains to the console (stdout), similar to running cat file | wc -l.

The full path to the file to read will be provided as the first command-line argument. You do not need to make your own test file. 

-------------------------------------------------------------------------------

## HINTS

To perform a filesystem operation you are going to need the fs module from the Node core library. To load this kind of module, or any other "global" module, use the following incantation:

    var fs = require('fs')

Now you have the full fs module available in a variable named fs.

All synchronous (or blocking) filesystem methods in the fs module end with 'Sync'. To read a file, you'll need to use fs.readFileSync('/path/to/file'). This method will return a Buffer object containing the complete contents of the file.

Documentation on the fs module can be found by pointing your browser here:
  file:///usr/local/lib/node_modules/learnyounode/node_apidoc/fs.html

Buffer objects are Node's way of efficiently representing arbitrary arrays of data, whether it be ascii, binary or some other format. Buffer objects can be converted to strings by simply calling the toString() method on them. e.g. var str = buf.toString().

Documentation on Buffers can be found by pointing your browser here:
  file:///usr/local/lib/node_modules/learnyounode/node_apidoc/buffer.html

If you're looking for an easy way to count the number of newlines in a string, recall that a JavaScript String can be .split() into an array of substrings and that '\n' can be used as a delimiter. Note that the test file does not have a newline character ('\n') at the end of the last line, so using this method you'll end up with an array that has one more element than the number of newlines.

-------------------------------------------------------------------------------

 » To print these instructions again, run: learnyounode print
 » To execute your program in a test environment, run: learnyounode run program.js
 » To verify your program, run: learnyounode verify program.js
 » For help run: learnyounode help


Peters-iMac:~ peterdarcy$ cd nodeLearning
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
NaN
Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   "NaN"                               !=    "15"                               
   ""                                  ==    ""                                 

────────────────────────────────────────────────────────────────────────────────

✗ Submission results did not match expected!
✓ Used synchronous method: fs.readFileSync()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js
/Users/peterdarcy/nodeLearning/node2.js:4
console.log(buf.toString().split('\n').lenght-1);
               ^
TypeError: Cannot read property 'toString' of undefined
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:4:16)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Module.require (module.js:365:17)
    at require (module.js:384:17)
    at Object.<anonymous> (/usr/local/lib/node_modules/learnyounode/node_modules/workshopper-wrappedexec/exec-wrap.js:87:3)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   ""                                  !=    "39"                               
                                       !=    ""                                 

────────────────────────────────────────────────────────────────────────────────

✗ Submission results did not match expected!
✗ Used asynchronous method: fs.readFile()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   "NaN"                               !=    "5"                                
   ""                                  ==    ""                                 

────────────────────────────────────────────────────────────────────────────────

✗ Submission results did not match expected!
✓ Used synchronous method: fs.readFileSync()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js
fs.js:500
  return binding.open(pathModule._makeLong(path), stringToFlags(flags), mode);
                 ^
TypeError: path must be a string
    at TypeError (native)
    at Object.fs.openSync (fs.js:500:18)
    at Object.fs.(anonymous function) [as openSync] (/usr/local/lib/node_modules/learnyounode/exercises/my_first_io/wrap.js:30:19)
    at Object.fs.readFileSync (fs.js:352:15)
    at Object.fs.(anonymous function) [as readFileSync] (/usr/local/lib/node_modules/learnyounode/exercises/my_first_io/wrap.js:30:19)
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:3:14)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   ""                                  !=    "39"                               
                                       !=    ""                                 

────────────────────────────────────────────────────────────────────────────────

✗ Submission results did not match expected!
✓ Used synchronous method: fs.readFileSync()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
NaN
Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   "NaN"                               !=    "9"                                
   ""                                  ==    ""                                 

────────────────────────────────────────────────────────────────────────────────

✗ Submission results did not match expected!
✓ Used synchronous method: fs.readFileSync()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   "NaN"                               !=    "25"                               
   ""                                  ==    ""                                 

────────────────────────────────────────────────────────────────────────────────

✗ Submission results did not match expected!
✓ Used synchronous method: fs.readFileSync()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js
/Users/peterdarcy/nodeLearning/node2.js:7
console.log(file.split('\n').length - 1);
                 ^
TypeError: undefined is not a function
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:7:18)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Module.require (module.js:365:17)
    at require (module.js:384:17)
    at Object.<anonymous> (/usr/local/lib/node_modules/learnyounode/node_modules/workshopper-wrappedexec/exec-wrap.js:87:3)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   ""                                  !=    "42"                               
                                       !=    ""                                 

────────────────────────────────────────────────────────────────────────────────

✗ Submission results did not match expected!
✓ Used synchronous method: fs.readFileSync()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
/Users/peterdarcy/nodeLearning/node2.js:7
console.log(file.split('\n').length - 1);
                 ^
TypeError: undefined is not a function
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:7:18)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
/Users/peterdarcy/nodeLearning/node2.js:7
console.log(file = file.split('\n').length - 1;);
                                              ^
SyntaxError: Unexpected token ;
    at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
/Users/peterdarcy/nodeLearning/node2.js:7
console.log(file.split('\n').length - 1;);
                                       ^
SyntaxError: Unexpected token ;
    at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
/Users/peterdarcy/nodeLearning/node2.js:7
console.log(file.split('\n').length - 1);
                 ^
TypeError: undefined is not a function
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:7:18)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
/Users/peterdarcy/nodeLearning/node2.js:7
console.log(file.split('\n').length - 1);
                 ^
TypeError: undefined is not a function
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:7:18)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
3
Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   "35"                                ==    "35"                               
   ""                                  ==    ""                                 

────────────────────────────────────────────────────────────────────────────────

✓ Submission results match expected
✗ Used asynchronous method: fs.readFile()

# FAIL

Your solution to MY FIRST I/O! didn't pass. Try again!

Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
fs.js:345
    throw new TypeError('Bad arguments');
          ^
TypeError: Bad arguments
    at Object.fs.readFileSync (fs.js:345:11)
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:5:11)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
/Users/peterdarcy/nodeLearning/node2.js:4
console.log(file.split('\n').length-1);
                 ^
TypeError: undefined is not a function
    at Object.<anonymous> (/Users/peterdarcy/nodeLearning/node2.js:4:18)
    at Module._compile (module.js:460:26)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
23
Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   "14"                                ==    "14"                               
   ""                                  ==    ""                                 

────────────────────────────────────────────────────────────────────────────────

✓ Submission results match expected
✓ Used synchronous method: fs.readFileSync()

# PASS

Your solution to MY FIRST I/O! passed!

Here's the official solution in case you want to compare notes:

────────────────────────────────────────────────────────────────────────────────
    var fs = require('fs')
    
    var contents = fs.readFileSync(process.argv[2])
    var lines = contents.toString().split('\n').length - 1
    console.log(lines)
    
    // note you can avoid the .toString() by passing 'utf8' as the
    // second argument to readFileSync, then you'll get a String!
    //
    // fs.readFileSync(process.argv[2], 'utf8').split('\n').length - 1

────────────────────────────────────────────────────────────────────────────────

You have 10 challenges left.
Type 'learnyounode' to show the menu.

Peters-iMac:nodeLearning peterdarcy$ learnyounode run node2.js
7
Peters-iMac:nodeLearning peterdarcy$ learnyounode verify node2.js

Your submission results compared to the expected:

                 ACTUAL                                 EXPECTED                
────────────────────────────────────────────────────────────────────────────────

   "19"                                ==    "19"                               
   ""                                  ==    ""                                 

────────────────────────────────────────────────────────────────────────────────

✓ Submission results match expected
✓ Used synchronous method: fs.readFileSync()

# PASS

 LEARN YOU THE NODE.JS FOR MUCH WIN!
─────────────────────────────────────
 MY FIRST ASYNC I/O!
 Exercise 4 of 13

Write a program that uses a single asynchronous filesystem operation to read a file and print the number of newlines it contains to the console (stdout), similar to running cat file | wc -l.

The full path to the file to read will be provided as the first command-line argument.

-------------------------------------------------------------------------------

# HINTS

The solution to this problem is almost the same as the previous problem except you must now do it the Node.js way: asynchronous.

Instead of fs.readFileSync() you will want to use fs.readFile() and instead of using the return value of this method you need to collect the value from a callback function that you pass in as the second argument. To learn more about callbacks, check out: [https://github.com/maxogden/art-of-node#callbacks](https://github.com/maxogden/art-of-node#callbacks).

Peters-iMac:nodeLearning peterdarcy$ cd ..
Peters-iMac:~ peterdarcy$ sudo npm install -g git-it
Password:
npm WARN engine github-oauth@0.0.4: wanted: {"node":"v0.8.x"} (current: {"node":"0.12.7","npm":"2.11.3"})
npm WARN deprecated CSSselect@0.4.1: the module is now available as 'css-select'
npm WARN deprecated CSSwhat@0.4.7: the module is now available as 'css-what'
/usr/local/bin/git-it -> /usr/local/lib/node_modules/git-it/git-it.js
git-it@1.6.8 /usr/local/lib/node_modules/git-it
├── marked@0.3.5
├── github-oauth@0.0.4 (request@2.12.0)
├── glob@3.2.11 (inherits@2.0.1, minimatch@0.3.0)
├── concat-stream@1.2.1 (bops@0.0.6)
├── ecstatic@0.5.8 (mime@1.3.4, minimist@1.1.3, he@0.5.0)
├── request@2.30.0 (aws-sign2@0.5.0, forever-agent@0.5.2, qs@0.6.6, tunnel-agent@0.3.0, oauth-sign@0.3.0, json-stringify-safe@5.0.1, mime@1.2.11, node-uuid@1.4.3, tough-cookie@0.9.15, http-signature@0.10.1, form-data@0.1.4, hawk@1.0.0)
├── cheerio@0.17.0 (entities@1.1.1, dom-serializer@0.0.1, lodash@2.4.2, htmlparser2@3.7.3, CSSselect@0.4.1)
├── workshopper-jlord@0.0.6 (map-async@0.1.1, tuple-stream@0.0.2, through@2.3.8, split@0.2.10, mkdirp@0.3.5, colors-tmpl@0.1.1, terminal-menu@0.2.0, xtend@2.1.2, optimist@0.6.1, msee@0.1.1)
└── handlebars@2.0.0 (optimist@0.3.7, uglify-js@2.3.6)
Peters-iMac:~ peterdarcy$ npm install -g git-it
npm ERR! Darwin 14.3.0
npm ERR! argv "node" "/usr/local/bin/npm" "install" "-g" "git-it"
npm ERR! node v0.12.7
npm ERR! npm  v2.11.3
npm ERR! path /usr/local/bin/git-it
npm ERR! code EACCES
npm ERR! errno -13

npm ERR! Error: EACCES, unlink '/usr/local/bin/git-it'
npm ERR!     at Error (native)
npm ERR!  { [Error: EACCES, unlink '/usr/local/bin/git-it'] errno: -13, code: 'EACCES', path: '/usr/local/bin/git-it' }
npm ERR! 
npm ERR! Please try running this command again as root/Administrator.
npm ERR! error rolling back Error: EACCES, unlink '/usr/local/bin/git-it'
npm ERR! error rolling back     at Error (native)
npm ERR! error rolling back  { [Error: EACCES, unlink '/usr/local/bin/git-it'] errno: -13, code: 'EACCES', path: '/usr/local/bin/git-it' }

npm ERR! Please include the following file with any support request:
npm ERR!     /Users/peterdarcy/npm-debug.log
Peters-iMac:~ peterdarcy$ sudo npm install -g git-it
npm WARN engine github-oauth@0.0.4: wanted: {"node":"v0.8.x"} (current: {"node":"0.12.7","npm":"2.11.3"})
npm WARN deprecated CSSselect@0.4.1: the module is now available as 'css-select'
npm WARN deprecated CSSwhat@0.4.7: the module is now available as 'css-what'
/usr/local/bin/git-it -> /usr/local/lib/node_modules/git-it/git-it.js
git-it@1.6.8 /usr/local/lib/node_modules/git-it
├── marked@0.3.5
├── github-oauth@0.0.4 (request@2.12.0)
├── concat-stream@1.2.1 (bops@0.0.6)
├── ecstatic@0.5.8 (mime@1.3.4, minimist@1.1.3, he@0.5.0)
├── glob@3.2.11 (inherits@2.0.1, minimatch@0.3.0)
├── cheerio@0.17.0 (entities@1.1.1, lodash@2.4.2, dom-serializer@0.0.1, CSSselect@0.4.1, htmlparser2@3.7.3)
├── workshopper-jlord@0.0.6 (map-async@0.1.1, tuple-stream@0.0.2, split@0.2.10, through@2.3.8, mkdirp@0.3.5, colors-tmpl@0.1.1, terminal-menu@0.2.0, optimist@0.6.1, xtend@2.1.2, msee@0.1.1)
├── handlebars@2.0.0 (optimist@0.3.7, uglify-js@2.3.6)
└── request@2.30.0 (aws-sign2@0.5.0, forever-agent@0.5.2, qs@0.6.6, tunnel-agent@0.3.0, oauth-sign@0.3.0, json-stringify-safe@5.0.1, mime@1.2.11, node-uuid@1.4.3, tough-cookie@0.9.15, hawk@1.0.0, form-data@0.1.4, http-signature@0.10.1)

                                                                       
    GIT + GITHUB : VERSION CONTROL + SOCIAL CODING                     
    -----------------------------------------------------------------  
    » GET GIT                                                          
    » REPOSITORY                                                       
    » COMMIT TO IT                                                     
    » GITHUBBIN                                                        
    » REMOTE CONTROL                                                   
    » FORKS AND CLONES                                                 
    » BRANCHES AREN'T JUST FOR BIRDS                                   
    » IT'S A SMALL WORLD                                               
    » PULL, NEVER OUT OF DATE                                          
    » REQUESTING YOU PULL, PLEASE                                      
    » MERGE TADA!                                                      
    -----------------------------------------------------------------  
    HELP                                                               
    EXIT                                                               
                                                                       

  #####################################################################
  ##                         ~~  GET GIT  ~~                         ##

                                                                       
    GIT + GITHUB : VERSION CONTROL + SOCIAL CODING                     
    -----------------------------------------------------------------  
    » GET GIT                                                          
    » REPOSITORY                                                       
    » COMMIT TO IT                                                     
    » GITHUBBIN                                                        
    » REMOTE CONTROL                                                   
    » FORKS AND CLONES                                                 
    » BRANCHES AREN'T JUST FOR BIRDS                                   
    » IT'S A SMALL WORLD                                               
    » PULL, NEVER OUT OF DATE                                          
    » REQUESTING YOU PULL, PLEASE                                      
    » MERGE TADA!                                                      
    -----------------------------------------------------------------  
    HELP                                                               
    EXIT                                                               
                                                                       

  #####################################################################

                                                                       
    GIT + GITHUB : VERSION CONTROL + SOCIAL CODING                     
    -----------------------------------------------------------------  
    » GET GIT                                                          
    » REPOSITORY                                                       
    » COMMIT TO IT                                                     
    » GITHUBBIN                                                        
    » REMOTE CONTROL                                                   
    » FORKS AND CLONES                                                 
    » BRANCHES AREN'T JUST FOR BIRDS                                   
    » IT'S A SMALL WORLD                                               
    » PULL, NEVER OUT OF DATE                                          
    » REQUESTING YOU PULL, PLEASE                                      
    » MERGE TADA!                                                      
    -----------------------------------------------------------------  
    HELP                                                               
    EXIT                                                               
                                                                       

  #####################################################################
  ##                         ~~  GET GIT  ~~                         ##
  #####################################################################

  Install Git on your computer and configure your name and email.

  Use the guide (see below) for step-by-step instructions.

  ---------------------------------------------------------------------

  » To verify your work for this problem, run: `git-it verify`.
  » Run `git-it` again to launch menu & go onto next challenge

  GUIDE

  » Open the guide in your browser: jlord.github.io/git-it
  » Traditional Chinese guide: jlord.github.io/git-it/index-zhtw.html

  » To view guide offline, copy this address to your browser:
  » /usr/local/lib/node_modules/git-it/guide/index.html 
  » /usr/local/lib/node_modules/git-it/guide/index-zhtw.html


Peters-iMac:~ peterdarcy$ git --version
xcode-select: note: no developer tools were found at '/Applications/Xcode.app', requesting install. Choose an option in the dialog to download the command line developer tools.
Peters-iMac:~ peterdarcy$ git version
git version 2.3.2 (Apple Git-55)

                                                                       
    GIT + GITHUB : VERSION CONTROL + SOCIAL CODING                     
    -----------------------------------------------------------------  
    » GET GIT                                             [COMPLETED]  
    » REPOSITORY                                                       
    » COMMIT TO IT                                                     
    » GITHUBBIN                                                        
    » REMOTE CONTROL                                                   
    » FORKS AND CLONES                                                 
    » BRANCHES AREN'T JUST FOR BIRDS                                   
    » IT'S A SMALL WORLD                                               
    » PULL, NEVER OUT OF DATE                                          
    » REQUESTING YOU PULL, PLEASE                                      
    » MERGE TADA!                                                      
    -----------------------------------------------------------------  
    HELP                                                               
    EXIT                                                               
                                                                       

  #####################################################################
  ##                       ~~  REPOSITORY  ~~                        ##
  #####################################################################

  Create a new Git repository on your computer.

  Use the guide (see below) for step-by-step instructions.

  ---------------------------------------------------------------------

  » To verify your work for this problem, run: `git-it verify`.
  » Run `git-it` again to launch menu & go onto next challenge

  GUIDE

  » Open the guide in your browser: jlord.github.io/git-it
  » Traditional Chinese guide: jlord.github.io/git-it/index-zhtw.html

  » To view guide offline, copy this address to your browser:
  » /usr/local/lib/node_modules/git-it/guide/index.html 
  » /usr/local/lib/node_modules/git-it/guide/index-zhtw.html


Peters-iMac:~ peterdarcy$ mkdir hello-world
Peters-iMac:~ peterdarcy$ cd hello-world
Peters-iMac:hello-world peterdarcy$ git init
Initialized empty Git repository in /Users/peterdarcy/hello-world/.git/
Peters-iMac:hello-world peterdarcy$ git status

                                                                       
    GIT + GITHUB : VERSION CONTROL + SOCIAL CODING                     
    -----------------------------------------------------------------  
    » GET GIT                                             [COMPLETED]  
    » REPOSITORY                                          [COMPLETED]  
    » COMMIT TO IT                                                     
    » GITHUBBIN                                                        
    » REMOTE CONTROL                                                   
    » FORKS AND CLONES                                                 
    » BRANCHES AREN'T JUST FOR BIRDS                                   
    » IT'S A SMALL WORLD                                               
    » PULL, NEVER OUT OF DATE                                          
    » REQUESTING YOU PULL, PLEASE                                      
    » MERGE TADA!                                                      
    -----------------------------------------------------------------  
    HELP                                                               
    EXIT                                                               
                                                                       

  #####################################################################
  ##                      ~~  COMMIT TO IT  ~~                       ##
  #####################################################################

  Create a file in your new repository, add something to that file
  and commit those changes to Git.

  Use the guide (see below) for step-by-step instructions.

  ---------------------------------------------------------------------

  » To verify your work for this problem, run: `git-it verify`.
  » Run `git-it` again to launch menu & go onto next challenge

  GUIDE

  » Open the guide in your browser: jlord.github.io/git-it
  » Traditional Chinese guide: jlord.github.io/git-it/index-zhtw.html

  » To view guide offline, copy this address to your browser:
  » /usr/local/lib/node_modules/git-it/guide/index.html 
  » /usr/local/lib/node_modules/git-it/guide/index-zhtw.html


Peters-iMac:hello-world peterdarcy$ cd hello-world
-bash: cd: hello-world: No such file or directory
Peters-iMac:hello-world peterdarcy$ nano

  GNU nano 2.0.6                New Buffer                            Modified  

hello



















^G Get Help  ^O WriteOut  ^R Read File ^Y Prev Page ^K Cut Text  ^C Cur Pos
^X Exit      ^J Justify   ^W Where Is  ^V Next Page ^U UnCut Text^T To Spell
