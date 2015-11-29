1. async
  1. why async
  1. asysn != multithread
  1. singlethread != sync
1. event
1. callback
  1. callback != async
    ```javascript
    var arr = [0];
    arr.forEach(function() {
      console.log(1);
    });
    console.log(2);
    
    setTimeout(function() {
      console.log(1);
    });
    console.log(2);
    ```
    
1. setTimeout
  1. tasks are queued
  1. tasks won't be executed until sync codes are finished
  1. the delay time is not guaranteed
  1. setInterval [http://javascript.info/tutorial/settimeout-setinterval](http://javascript.info/tutorial/settimeout-setinterval)
  
1. promise
  ```javascript
  var promise = new Promise(function(resolve, reject) {
    setTimeout(function() {
      var a = 1;
      if (a == 2) {
        resolve('{"a":1}');
      }
      else {
        reject({a:2});
      }
    }, 1000);
  });
  
  function stringify() {
    return JSON.stringify(arguments[0]);
  }
  
  promise.then(JSON.parse, stringify).then(function(result) {
    console.log(result);
  }, function(err) {
    console.log(err);
  });
  ```
