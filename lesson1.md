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
	[http://en.wikipedia.org/wiki/Web_browser_engine](http://en.wikipedia.org/wiki/Web_browser_engine) 	[http://baike.baidu.com/view/1369399.htm](http://baike.baidu.com/view/1369399.htm)
	1. mobile: webkit only
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
1. CSS 	[https://adactio.com/journal](https://adactio.com/journal)
1. JavaScript
	1. Object: dynamic, HashMap
		1. built-in objects. JSON, Math, Date, RegExp, Object, String, Number, Array, Function etc.
		1. create object
'''javascript
{}
var person = { };
var person = {
    name: ‘Tom’,
    age: 14,
    talk: function() {
    }
};
'''
new Object();
Object.create();
JSON: serialization
retrieval & set
property name: $, _, a-z, A-Z, 0-9
person.name, person[‘name’]
delete property vs set undefined
configurable
enumeration
in
for in
Object.keys
Misc
namespace: avoid global variables
window, global
doc only /** ... */
Array
special object
automatically maintain length property
iteration
for (var i=0; i<length; i++) { }
while(length--) { }
for (i in array) { }
forEach
methods
isArray: static
push
concat
sort: unstable
indexOf/lastIndexOf
slice: clone
splice
insert & delete
difference from delete
join/reverse/pop/reduce
Array-Like Objects
dom methods, arguments
convert to real array
String
readonly array-like objects
array methods on string
new String() vs ""
methods
Function
constructor class
define functions
function foo() {}
var foo = function() {}
(function() {})()
hoisting
scope
what’s this?
change scope
function.call/apply(obj, arg)
obj.foo = func;
arguments
callee/caller
closure
prototype
Misc
===, !==
number: float 0.1+0.2 != 0.3
CSS
style
class
css selector
pseudo class & pseudo element
layout
display property
position property
box model
css3

