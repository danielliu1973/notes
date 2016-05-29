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

1. scope/context
  ```html
  <button onclick="save()">Save</button>
  ```
  not equals to
  ```javascript
  button.onclick = function() {
    save();
  };
  ```
  
  ```html
  <button onclick="save(event, this)">Save</button>
  ```
  equals to
  ```javascript
  button.onclick = function(event) {
    save(event, this);  // this === button
  };
  ```
  
  ```javascript
  var person = {
    name: 'Tom',
    sayName: function() {
      return this.name;
    }
  };
  button.onclick = person.sayName;
  button.onclick = person.sayName.bind(person);
  button.onclick = function() {
    person.sayName();
  };
  ```

1. event.preventDefault & return false
  ```html
  <input type="checkbox" id="mycheck">check
  ```
  ```javascript
  function go(event) {
    event.preventDefault();
  };
  //document.getElementById('myanchor').addEventListener('click', go);
  document.getElementById('mycheck').addEventListener('click', go);
  ```
  
  ```html
  <a id="myanchor" href="#">go</a>
  ```
  ```javascript
    document.getElementById('myanchor').addEventListener('click', function(event) {
      alert('do my stuff');
      event.preventDefault();
    });
  ```
  ```html
  <input id="myname">
  ```
  ```javascript
  document.getElementById('myname').addEventListener('keydown', function(event) {
    event = event || window.event;
    var charCode = (typeof event.which == "undefined") ? event.keyCode : event.which;
    if (!((charCode >= 65 && charCode <= 90) || (charCode >= 97 && charCode <= 122))) {
      event.preventDefault();
    }
  });
  ```

1. event.stopPropagation & return false
  ```html
  <a href="#" id="myanchor">go</a>
  ```
  ```javascript
  document.getElementById('myanchor').addEventListener('click', function(event) {
    alert('click anchor');
    event.stopPropagation();
    return false;
  });
  document.body.addEventListener('click', function() {
    alert('click body');
  });
  ```
  
1. performance
  1. cancel bubble
  1. avoid too many event handlers
  ```html
  <div id="buttons">
    <button id="ok">ok</button>
    <button id="cancel">cancel</button>
  </div>
  ```
  ```javascript
  document.getElementById('buttons').onclick = function (event) {
    var id = event.target.id;
    if (id === 'ok') {
      alert('do ok');
    } else if (id === 'cancel') {
      alert('do cancel');
    }
  };
  ```
  
  1. setTimeout

1. [good artice](https://www.smashingmagazine.com/2013/11/an-introduction-to-dom-events/)

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
