#Go over
1. Function
    1. hoisting
    1. scope
    1. context
1. MVC
#New
1. Function
    1. closure
        1. [http://www.w3schools.com/js/js_function_closures.asp](http://www.w3schools.com/js/js_function_closures.asp)
    1. prototype
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
    1. Element & Container
    1. Form