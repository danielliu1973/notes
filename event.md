1. DOM event [http://www.w3schools.com/jsref/dom_obj_event.asp](http://www.w3schools.com/jsref/dom_obj_event.asp)
  1. attach event
    ```javascript
    document.onclick = function() { // must be lower cased
      alert('document clicked');
    };
    ```
    
    ```html
    <!-- event attribute is case insensative -->
    <body onclick="alert('clicked')">
    </body>
    ```
  2. addEventListener
    ```javascript
    document.addEventListener('click', function() {
        console.log('document clicked');
    });
    ```
    
  3. removeEventListener
    ```javascript
    var func = function() {
        console.log('received 2');
    };
    document.addEventListener('click', func);
    document.removeEventListener('click', func);
    ```
    
  4. dispatchEvent
    ```javascript
    document.addEventListener('click', function() {
        console.log('document clicked');
    });
    document.dispatchEvent(new Event('click'));
    ```
    
  5. useCapture & bubble [http://jsfiddle.net/ading/72ghycxz/](http://jsfiddle.net/ading/72ghycxz/)
  ```html
  <div id="parent" style="border: 10px solid red" onclick="alert(1)">
    <div id="children" style="border: 10px solid black">
        Click
    </div>
  </div>
  ```
  
  ```javascript
  var parent = document.getElementById('parent'),
    children = document.getElementById('children');

  children.addEventListener('click', function (e) { 
      alert('Children Capture on ' + e.currentTarget.id);
      // e.stopPropagation();
  }, true);
  
  children.addEventListener('click', function (e) { 
      alert('Children Bubble on ' + e.currentTarget.id);
      // e.stopPropagation();
  }, false);
  
  parent.addEventListener('click', function (e) { 
      alert('Parent Capture on ' + e.currentTarget.id);
      // e.stopPropagation();
  }, true);
  
  parent.addEventListener('click', function (e) { 
      alert('Parent Bubble on ' + e.currentTarget.id);
      // e.stopPropagation();
  }, false);
  ```

  6. custom event [https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Creating_and_triggering_events](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Creating_and_triggering_events)
  
1. AngularJS event [https://docs.angularjs.org/guide/scope](https://docs.angularjs.org/guide/scope)

    ```javascript
    angular.module('eventExample', [])
      .controller('EventController', ['$scope', function($scope) {
        $scope.count = 0;
        $scope.$on('MyEvent', function() {
          $scope.count++;
        });
          
        //$emit('MyEvent');
        //$broadcast('MyEvent');
      }]);
    ```

1. DOM event & ng event
  ```javascript
  var inboundEvents = [
    'logInRequest',
    'logOutRequest'
  ], outboundEvents = [
    'loggedIn',
    'loggedOut',
    'loginError'
  ];
    
  inboundEvents.forEach(function(name) {
    $document.on(name, function(e) {
      $rootScope.$broadcast(name, e.detail);
    });
  });

  outboundEvents.forEach(function(name) {
    $rootScope.$on(name, function(e, detail) {
      var ce = document.createEvent('CustomEvent');
      ce.initCustomEvent(name, true, true, detail || {});
      document.dispatchEvent(ce);
    });
  });
  ```

1. postMessage [https://developer.mozilla.org/en/docs/Web/API/Window/postMessage](https://developer.mozilla.org/en/docs/Web/API/Window/postMessage)
