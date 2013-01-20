# Google Code Prettify

Direct port of svn into git from http://google-code-prettify.googlecode.com/svn/trunk/

## Install

via [Bower](http://twitter.github.com/bower/)

	bower install google-code-prettify

or [Yeoman](http://yeoman.io/)

	yeoman install google-code-prettify


## Usage

The prettify script is AMD compatible and can be used modularly. Here is an example of it using RequireJS:

	define(['jquery', 'prettify'], function($, prettify){
		var code = '';
		$('pre').addClass('prettyprint').each(function(idx, el){
				code = el.firstChild;
				code.innerHTML = prettify.prettyPrintOne(code.innerHTML);
			})
		);
	});

Or it may just be used in a global context like the following:

	(function(){
		$('pre').addClass('prettyprint');
		prettyPrint();
	})();

More information can be found in the original [README.html](http://google-code-prettify.googlecode.com/svn/trunk/README.html)