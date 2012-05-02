#PHP to Console#
This project consists of a small PHP class and a Node.js app. I, Kevin, is mainly into PHP but have also been playing with Node.js. When I debug my PHP I noramly print_r or echo out variables to debug. This can get messy. I wanted a cross platform application to show output from PHP to help debug. Node.js runs on Windows, Mac and Linux, just like PHP, so it's a great choice.

So that's all it does for now and a really simple comand line to quit, help, check version and clear. But I might try to add what's in the "Some Ideas" section towards the end of this readme.

##How to use##
**Node.js Start**<br>
CD in Terminal or cmd.exe to the node folder with this download and type app.js and it will start on port 5088, if you want to change it edit `var port = 5088;` in the app.js towards the top.

**PHP**<br>
in the php folder copy `php2console.php` in to your PHP project folder and use the following exmaple.

spellcheck

Then type

	<?php
		require 'php2console.php';
		$php_console = new php_console('localhost', '5088');
		$php_console->output('OMG! AN ERROR!');
	?>

**Dependencies**<br>

**PHP:** CURL

**Node.js:** [express](http://expressjs.com/ "express"), but it's included in the `node_modules` to ensure we're both on the same version, if you need to reinstall type `npm install express`.

##License##
Everything except the contents of `node_modules`(each module will most likey have it's own license) is under the license in the inclued LICENSE.txt file.

##Some Ideas##
**Profiling:**

- Profiling (save to a SQLite DB)
- Profile log (mini web app built in the node code)


**Companion script(should NOT be used on production, only when devloping):**

- Companion PHP script for the command line to connect to.
- Run SQL from the command line
- get phpinfo()
- list modules
- list module info
- list modules version 
