1. IDE
	1. Brackets: [http://brackets.io/] I'm using it. Recommended.
	1. WebStorm: [https://www.jetbrains.com/webstorm/]() It's the best, but you'll need a license.
	1. Eclipse: [http://eclipse.org/webtools/]() not bad. Used to be very popular.
1. VCS
	1. Create an account @ [https://bitbucket.org/]() and [https://github.com/]()
	1. download SourceTree @ [http://www.sourcetreeapp.com/]() if you don't know how to do it, I'll help you out in the class.
1. Server
	1. install Apache server [http://www.apachehaus.com/]() optional for now
	1. or use your existing http server (IIS, tomcat etc.)
1. Browsers
	1. 5 major browsers. IE, FireFox, Chrome, Safari, Opera
3 (or 4) Layout Engines (kernel, rendering engines): Webkit (Blink), Trident, Gecko
use UA (User Agent) to detect browser type and layout engine http://www.whatismybrowser.com/ 
resources http://en.wikipedia.org/wiki/Web_browser_engine http://baike.baidu.com/view/1369399.htm
mobile: webkit only
HTML
doctype
xml: tag match, case insensitive
meta: viewport
SEO
single quote, double quote, no quote
html5 tags http://www.w3schools.com/html/html5_intro.asp
form input type http://www.w3schools.com/html/html_form_input_types.asp
semantic tags: header, footer
local storage
canvas
server-side rendering vs client-side rendering
CSS https://adactio.com/journal
JavaScript
Object: dynamic, HashMap
built-in objects. JSON, Math, Date, RegExp, Object, String, Number, Array, Function etc.
create object
{}
var person = { };
var person = {
    name: ‘Tom’,
    age: 14,
    talk: function() {
    }
};
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

