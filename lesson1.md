1. IDE
	1. Brackets: [http://brackets.io/](http://brackets.io/) I'm using it. Recommended.
	1. WebStorm: [https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/) It's the best, but you'll need a license.
	1. Eclipse: [http://eclipse.org/webtools/](http://eclipse.org/webtools/) not bad. Used to be very popular.
1. VCS
	1. Create an account @ [https://bitbucket.org/](https://bitbucket.org/) and [https://github.com/](https://github.com/)
	1. download SourceTree @ [http://www.sourcetreeapp.com/](http://www.sourcetreeapp.com/) if you don't know how to do it, I'll help you out in the class.
1. Server
	1. install Apache server [http://www.apachehaus.com/](http://www.apachehaus.com/) optional for now
	1. or use your existing http server (IIS, tomcat etc.)
1. Browsers
	1. 5 major browsers. IE, FireFox, Chrome, Safari, Opera
	1. 3 (or 4) Layout Engines (kernel, rendering engines): Webkit (Blink), Trident, Gecko
	1. use UA (User Agent) to detect browser type and layout engine
	[http://www.whatismybrowser.com/](http://www.whatismybrowser.com/)
	1. resources
		- [http://en.wikipedia.org/wiki/Web_browser_engine](http://en.wikipedia.org/wiki/Web_browser_engine)
		- [http://baike.baidu.com/view/1369399.htm](http://baike.baidu.com/view/1369399.htm)
	1. mobile: webkit only
1. Resources
	1. [http://www.w3schools.com/](http://www.w3schools.com/)
	1. [https://developer.mozilla.org/en-US/docs/Web](https://developer.mozilla.org/en-US/docs/Web)
	1. [http://www.51zxw.net/list.aspx?cid=393](http://www.51zxw.net/list.aspx?cid=393)
1. HTML
	1. doctype
	1. xml: tag match, case insensitive
	1. meta: viewport
	1. SEO
	1. single quote, double quote, no quote
	1. html5 tags http://www.w3schools.com/html/html5_intro.asp
		1. form input type http://www.w3schools.com/html/html_form_input_types.asp
		1. semantic tags: header, footer
		1. local storage
		1. canvas
	1. server-side rendering vs client-side rendering
1. CSS
	- [https://adactio.com/journal](https://adactio.com/journal)
1. JavaScript
	1. Object: dynamic, HashMap
		1. built-in objects. JSON, Math, Date, RegExp, Object, String, Number, Array, Function etc.
		1. create object
			1. {}

```
				var person = {};
				
				var person = {
					name: ‘Tom’,
					age: 14,
					talk: function() {
					}
				};
```
			1. new Object();
			1. Object.create();
		1. JSON: serialization
		1. retrieval & set
			1. property name: $, _, a-z, A-Z, 0-9
			1. person.name, person[‘name’]
		1. delete property vs set undefined
			1. configurable
		1. enumeration
			1. in
			1. for in
			1. Object.keys
		1. Misc
			1. namespace: avoid global variables
			1. window, global
			1. doc only /** ... */
	1. Array
		1. special object
		1. automatically maintain length property
		1. iteration
			1. for (var i=0; i<length; i++) { }
			1. while(length--) { }
			1. for (i in array) { }
			1. forEach
		1. methods
			1. isArray: static
			1. push
			1. concat
			1. sort: unstable
			1. indexOf/lastIndexOf
			1. slice: clone
			1. splice
				1. insert & delete
				1. difference from delete
			1. join/reverse/pop/reduce
		1. Array-Like Objects
			1. dom methods, arguments
			1. convert to real array
	1. String
		1. readonly array-like objects
		1. array methods on string
		1. new String() vs ""
		1. methods
	1. Function
		1. constructor class
		1. define functions
			1. function foo() {}
			1. var foo = function() {}
			1. (function() {})()
		1. hoisting
		1. scope
			1. what’s this?
			1. change scope
				1. function.call/apply(obj, arg)
				1. obj.foo = func;
		1. arguments
			1. callee/caller
		1. closure
		1. prototype
	1. Misc
		1. ===, !==
		1. number: float 0.1+0.2 != 0.3
1. CSS
	1. style
	1. class
	1. css selector
	1. pseudo class & pseudo element
	1. layout
	1. display property
	1. position property
	1. box model
	1. css3

