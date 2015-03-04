#Go over
1. Function
    1. hoisting
    1. scope
    1. context
1. MVC
#New
1. Function
    1. closure
    1. prototype
1. Basics
    1. ajax
            // This is the client-side script.
 
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

    1. get vs post
1. ExtJS
    1. History
    1. Element & Container
    1. Form