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
Everything except the contents of `node_modules`(each module will most likey have it's own) is under the following license:

> Copyright (c) 2012, Kevin Whitman and Contributors
> All rights reserved. 
> 
> Redistribution and use in source and binary forms, with or without 
> modification, are permitted provided that the following conditions are met: 
> 
>  * Redistribution’s of source code must retain the above copyright notice, 
>    this list of conditions and the following disclaimer.
>  * Neither the name of Kevin Whitman nor the names of its contributors may be used to endorse or promote products derived from this software without specific 
>    prior written permission.
> 
> THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" 
> AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE 
> IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE 
> ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE 
> LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR 
> CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF 
> SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS 
> INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN 
> CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
> ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE 
> POSSIBILITY OF SUCH DAMAGE. 

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
