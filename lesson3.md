1. prototype
    1. prototype vs \__proto__

            function Person(name) {
                this.name = name;
            }
            Person.prototype.getName = function() {
                return this.name;
            };
            var person = new Person('Aaron');
            var person = {};
            Person.call(person, 'Aaron');
            person.__proto__ = Person.prototype;
            var p2 = new Person('Ding');

    1. inheritance

            var __extends = function (child, parent) {
                for (var p in parent) {
                    if (parent.hasOwnProperty(p)) child[p] = parent[p];
                }
                function __() { this.constructor = child; }
                __.prototype = parent.prototype;
                child.prototype = new __();
                //child.prototype = Object.create(parent.prototype);
                //child.prototype.constructor = child;
            };

            function Student(name, id) {
                Person.call(this, name);
                this.id = id;
            }

            __extends(Student, Person);

            Student.prototype.getId = function() {
                return this.id;
            };
    
    1. prototype chain (\__proto__ chain)
            var p = new Person();
            p.getName = function() {/*...*/};
            p.getName();

    1. instanceof
            Object.getPrototypeOf(obj) -> obj.__proto__  
            obj instanceof Clazz -> obj.\__proto\__ === Clazz.prototype || obj.\__proto__.__proto__ === Clazz.prototype
                
            var o = {};
            console.log(o instanceof Person);
            console.log(o instanceof Student);
            o.__proto__ = Student.prototype;

    1. Resources
        1.[http://www.w3schools.com/js/js_object_prototypes.asp](http://www.w3schools.com/js/js_object_prototypes.asp)
        1. [http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/](http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/)
        1. [http://www.crockford.com/javascript/inheritance.html](http://www.crockford.com/javascript/inheritance.html)
        1. [http://javascript.crockford.com/prototypal.html](http://javascript.crockford.com/prototypal.html)
        1. [http://openwares.net/js/javascript_prototype_chain.html](http://openwares.net/js/javascript_prototype_chain.html)
        1. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/prototype](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/prototype)
        1. [Object.create](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/create)
    
1. Basics
    1. ajax
        1. vanilla javascript

                // Initialize the Ajax request.
                var xhr = new XMLHttpRequest();
                xhr.open('get', 'send-ajax-data.php');
 
                // Track the state changes of the request.
                xhr.onreadystatechange = function () {
                    var DONE = 4; // readyState 4 means the request is done.
                    var OK = 200; // status 200 is a successful return.
                    if (xhr.readyState === DONE) {
                        if (xhr.status === OK) {
                            alert(xhr.responseText); // 'This is the returned text.'
                        } else {
                            alert('Error: ' + xhr.status); // An error occurred during the request.
                        }
                    }
                };
 
                // Send the request to send-ajax-data.php
                xhr.send(null);

        1. ExtJS

                Ext.Ajax.request({
                    url: 'ajax_demo/sample.json',
                    method: 'get',
                    params: {
                        key: value
                    },
                    success: function(response, opts) {
                        var obj = Ext.decode(response.responseText);
                        console.dir(obj);
                    },
                    failure: function(response, opts) {
                        console.log('server-side failure with status code ' + response.status);
                    }
                });

        1. AngularJS

                // Simple POST request example (passing data) :
                $http.post('/someUrl', {msg:'hello word!'}).
                  success(function(data, status, headers, config) {
                    // this callback will be called asynchronously
                    // when the response is available
                  }).
                  error(function(data, status, headers, config) {
                    // called asynchronously if an error occurs
                    // or server returns response with an error status.
                  });

      1. get vs post

1. ExtJS
    
    1. UI components
        1. Element & Container
        1. Layouts
            1. absolute, table
            1. fit, border, accordion, card
            1. auto, anchor, form, vbox
            1. hbox, column
    