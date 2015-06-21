1. prototype
    1. [http://www.w3schools.com/js/js_object_prototypes.asp](http://www.w3schools.com/js/js_object_prototypes.asp)
    1. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/prototype](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/prototype)
    1. [http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/](http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/)
    1. [http://www.crockford.com/javascript/inheritance.html](http://www.crockford.com/javascript/inheritance.html)
    1. [http://javascript.crockford.com/prototypal.html](http://javascript.crockford.com/prototypal.html)
    1. [http://openwares.net/js/javascript_prototype_chain.html](http://openwares.net/js/javascript_prototype_chain.html)
    1. prototype vs \__proto__

            function Person(first, last, age, eyecolor) {
                this.firstName = first;
                this.lastName = last;
                this.age = age;
                this.eyeColor = eyecolor;
            }
            Person.prototype.getFullName = function() {
                return this.firstName + " " + this.lastName;
            };

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
    1. History
    1. Development mode & production mode
    1. Sencha Command
    1. UI components
        1. Element & Container
        1. Layouts
            1. absolute, table
            1. fit, border, accordion, card
            1. auto, anchor, form, vbox
            1. hbox, column
    