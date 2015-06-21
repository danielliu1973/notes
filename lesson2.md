1. JavaScript
    1. var me = this, ths = this, self = this;
    1. !!foo
    1. foo = foo || {}
    1. forEach
    1. deferred/promise pattern
    1. nested function

1. closure
            
        Closures are functions that refer to independent (free) variables.

    1. Resources 
        1. [http://www.w3schools.com/js/js_function_closures.asp](http://www.w3schools.com/js/js_function_closures.asp)
        1. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
        1. [http://javascriptissexy.com/understand-javascript-closures-with-ease/](http://javascriptissexy.com/understand-javascript-closures-with-ease/)
    1. Conclusion
        1. function returns a function
        1. the function uses a local variable between the two functions
        
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

    1. closure in a loop

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
    1. Layout system
    1. Events
    1. Store, Model, Proxy, View
    1. [http://www.extjs-tutorial.com/extjs/naming-convention](http://www.extjs-tutorial.com/extjs/naming-convention)
