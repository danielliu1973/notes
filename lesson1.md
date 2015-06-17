1. Javascript development introduction
    1. self-study skills
    1. **server-side rendering vs client-side rendering**
1. Books & resources
    1. [http://it-ebooks.info](http://it-ebooks.info)
	1. [http://www.w3schools.com/](http://www.w3schools.com/)
	1. [https://developer.mozilla.org/en-US/docs/Web](https://developer.mozilla.org/en-US/docs/Web)
	1. [http://www.51zxw.net/list.aspx?cid=393](http://www.51zxw.net/list.aspx?cid=393)
1. IDE
	1. Brackets: [http://brackets.io/](http://brackets.io/)
	1. WebStorm: [https://www.jetbrains.com/webstorm/](https://www.jetbrains.com/webstorm/)
1. VCS
	1. Create an account @ [https://bitbucket.org/](https://bitbucket.org/) and [https://github.com/](https://github.com/)
	1. download SourceTree @ [http://www.sourcetreeapp.com/](http://www.sourcetreeapp.com/)
1. Server
	1. Apache server [http://www.apachehaus.com/](http://www.apachehaus.com/)
    1. NodeJS[https://nodejs.org/](https://nodejs.org/)
	1. or use your application server (IIS, tomcat etc.)
1. Browsers
	1. 5 major browsers. IE, FireFox, Chrome, Safari, Opera
	1. 3 (or 4) Layout Engines (kernel, rendering engines): Webkit (Blink), Trident, Gecko
	1. use UA (User Agent) to detect browser type and layout engine
        1. [extjs code](http://docs.sencha.com/extjs/5.1/5.1.1-apidocs/source/OS.html#Ext-os)
        1. [http://www.whatismybrowser.com/](http://www.whatismybrowser.com/)
	1. resources
		- [http://en.wikipedia.org/wiki/Web_browser_engine](http://en.wikipedia.org/wiki/Web_browser_engine)
		- [http://baike.baidu.com/view/1369399.htm](http://baike.baidu.com/view/1369399.htm)
	1. mobile: webkit only
1. HTML
	1. doctype
	1. meta: viewport
	1. html5 tags [http://www.w3schools.com/html/html5_intro.asp](http://www.w3schools.com/html/html5_intro.asp)
		1. form input type http://www.w3schools.com/html/html_form_input_types.asp
		1. semantic tags: header, footer
		1. local storage
		1. canvas
1. CSS [https://adactio.com/journal](https://adactio.com/journal)
    1. style
	1. class
	1. css selector
	1. pseudo class & pseudo element
	1. layout
	1. display property
	1. position property
	1. **box model**
	1. css3
1. JavaScript
    1. Basic Syntax
        1. var x = 1;
        1. data types : String, Number, Boolean, Array, Object
        1. value comparison, == vs ===, != vs !==
        
            [Equality_comparisons_and_sameness](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)
        
        1. operator +, -, *, /, %, ++, --, |, &
        1. function
                function sum(a, b) {
                    return a + b;
                }

        1. conditional statements: if, switch 
                var foo;
                if (foo) {
                    // ...
                }

        1. regex
        1. object
                var person = {};
                person.name = 'Tom';
                person.age = 10;

        1. array
                var arr = [1, 2, 3];
                arr.push(9);

        1. loop: for, while
        1. error handling
                try {
                    // ...
                } catch (e) {
                    // ...
                }
        
        1. strict mode: "use strict"

    1. Advanced
        1. Object: dynamic, HashMap
            1. built-in objects. JSON, Math, Date, RegExp, Object, String, Number, Array, Function etc.
                1. **[API](http://docs.sencha.com/extjs/4.2.2/#!/api)**
                1. [API@Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects)
            1. create object
                1. {}
                1. new Object();
                1. Object.create();
            1. JSON: serialization
            1. retrieval & set
                1. **property name: $, _, a-z, A-Z, 0-9**
                1. **person.name, person[‘name’]**
            1. window, global
            1. delete
                1. delete property vs set undefined
                
                        var obj = {
                            foo: 'a',
                            bar: 'b'
                        };
                        obj.foo = undefined;
                        console.log(obj.foo);
                        
                        delete obj.bar;
                        console.log(obj.bar);
                            
                1. configurable property

                        var foo = 'test';
                        delete window.foo;
                        window.bar = 'test';
                        delete window.bar;

            1. enumeration
                1. in
                1. for in
                
                        for (var key in object) {
                            console.log(key, object[key]);
                        }

                1. Object.keys
            1. Misc
                1. namespace: avoid global variables
                1. doc only [example](http://docs.sencha.com/extjs/4.2.2/source/Label2.html#Ext-form-Label)
                
                        var foo = {
                            id: 0,

                            /**
                             * name
                             */
                        };

        1. Array
            1. special object, automatically maintain length property
            1. iteration
                1. for (var i=0; i<length; i++) { }
                1. while(length--) { }
                1. for (i in array) { }
                1. **forEach**
            1. methods
                1. isArray: static
                1. push
                1. concat
                1. sort: unstable
                1. indexOf/lastIndexOf
                1. **slice**: clone
                1. splice
                    1. insert & delete
                    1. difference from delete
                1. join/reverse/pop/reduce
            1. **Array-Like Objects**
                1. dom methods, function arguments
                1. convert to real array

                            Array.prototype.slice.apply(arguments);

        1. String
            1. readonly array-like objects
            1. array methods on string
            
                            Array.prototype.method.apply(string);
            
            1. new String() vs ""
            1. methods
        1. Function
            1. constructor class
            1. **define functions**
            
                    function foo() {
                        // ...
                    }
                    var foo = function() {
                        // ...
                    };
                    (function() {
                        // ...
                    })();
                        
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

1. homework
    1. server-side rendering vs client-side rendering
    1. MVC
    1. implement function add(a, b, c...)
        add(3); // returns 3
        add(3, 4);  // returns 7
        add(3, 4, 5);  // returns 12
    1. impplement function max(a, b, c...)
        max(3); // returns 3
        max(3, 4);  // returns 4
        max(3, 4, 5);  // returns 5
    1. implement function clone
