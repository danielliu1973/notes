1. Learn from source code

1. variable scope [This is not an answer](http://stackoverflow.com/questions/500431/what-is-the-scope-of-variables-in-javascript)
    1. global
        
        ```javascript
        var myglobal = 432;
        console.log(window.myglobal);
        for (var key in window) {
            console.log(key);
        }
        console.log(key);
        ```

    1. function/local
        
        ```javascript
        function foo() {
            var local1 = 'local1',
                local2 = 'local2';
            function bar() {
                var local1 = 'another local';
                console.log(local1);
                console.log(local2);
            }
            console.log(local1);
            bar();
            console.log(local2);
        }
        ```
        
    3. let
        
        ```
        /*jshint esnext: true*/
        function letTest() {
            'use strict';
            let x = 31;
            if (true) {
              let x = 71;  // different variable
              console.log(x);  // 71
            }
            console.log(x);  // 31
        }

        letTest();
        ```
          
        test:
        
        ```
        var x = 5;

        function foo() {
            console.log(x);
            var x = 10;
            console.log(x); 
        }
        
        foo();
        ```

1. [hoisting](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)
    1. only declaration, not assignment
    1. function
1. [IIFE - immediately-invoked function expression](http://benalman.com/news/2010/11/immediately-invoked-function-expression/#iife)
    
    ```html
    <html>
      <head>
        <scipt>
          function winloaded() {
            alert('loaded');
          }
          window.onload = winloaded;
        </script>
      </head>
      <body>
      </body>
    </html>
    ```
    
    ```javascript
    (function() {
        // ...
    })();
    ```

1. [modular pattern](http://www.adequatelygood.com/JavaScript-Module-Pattern-In-Depth.html)
    
    ```typescript
    module victoria {
        export function myFunc() {
            console.log('victoria.myFunc');
        }
    }
    ```
    
    ```javascript
    var victoria;
    (function (victoria) {
        function myFunc() {
            console.log('victoria.myFunc');
        }
        victoria.myFunc = myFunc;
    })(victoria || (victoria = {}));
    ```

1. JavaScript
    1. var me = this, ths = this, self = this;
    1. !!foo
    1. foo = foo || {}
    1. forEach
    1. deferred/promise pattern
    1. nested function

1. closure
    
    ```        
    Closures are functions that refer to independent (free) variables.
    ```

    1. Resources 
        1. [http://www.w3schools.com/js/js_function_closures.asp](http://www.w3schools.com/js/js_function_closures.asp)
        1. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
        1. [http://javascriptissexy.com/understand-javascript-closures-with-ease/](http://javascriptissexy.com/understand-javascript-closures-with-ease/)
    1. Conclusion
        1. function returns a function
        1. the function uses a local variable between the two functions
        
        ```javascript
        function makeAdder(x) {
            return function(y) {
                return x + y;
            };
        }

        var add5 = makeAdder(5);
        var add10 = makeAdder(10);

        function foo(bar) {
            // ...
        }
        function foo() {
            var bar = arguments[0];
            // ...
        }
        ```

    1. closure in a loop

        ```javascript
        function showHelp(help) {
            document.getElementById('help').innerHTML = help;
        }

        function setupHelp() {
            var helpText = [
                {'id': 'email', 'help': 'Your e-mail address'},
                {'id': 'name', 'help': 'Your full name'},
                {'id': 'age', 'help': 'Your age (you must be over 16)'}
            ];

            for (var i = 0; i < helpText.length; i++) {
                var item = helpText[i];
                document.getElementById(item.id).onfocus = function() {
                    showHelp(item.help);
                }
            }
        }

        setupHelp();
        ```

        fix
        
        ```javascript
        for (var i = 0; i < helpText.length; i++) {
            var item = helpText[i];
            document.getElementById(item.id).onfocus = (function() {
                var help = item.help;
                return function() {
                    showHelp(help);
                };
            }());
        }
        ```
    
1. ExtJS
    1. Real examples
        1. [synology](https://www.synology.com/en-us/dsm/5.2/live_demo)
        1. [sitescout](https://rtb.sitescout.com/)
    1. History
    1. Development mode & production mode
    1. Sencha Command
	1. Examples:
		1. Forms, ComboBox, Grids, Windows, Layout Managers, Toolbars and Menus
		1. DataView
		1. Tabs, Trees
		1. Drag & Drop
	1. Class system
    1. [http://www.extjs-tutorial.com/extjs/naming-convention](http://www.extjs-tutorial.com/extjs/naming-convention)
    1. Layout system, component, containers
    1. Store, Model, Proxy, View
    1. Events
    1. rules
        1. no id
        1. no global functions
        1. no functions in strings
