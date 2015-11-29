1. async
1. event
1. callback
  1. callback != async
1. setTimeout
1. promise
  '''javascript
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
  '''