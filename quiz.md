1.
```javascript
 (function(x){
    delete x;
    return x;
  })(1);
```

2.
```javascript
  var foo = {
    bar: function() { return this.baz; },
    baz: 1
  };
  (function(){
    return typeof arguments[0]();
  })(foo.bar);
```

3.
```javascript
  var foo = {
    bar: function(){ return this.baz; },
    baz: 1
  };
  typeof (f = foo.bar)();
```

4.
```javascript
(function(foo){
    return typeof foo.bar;
  })({ foo: { bar: 1 } });
```

5.
```javascript
  var f = (function f(){ return "1"; }, function g(){ return 2; })();
  typeof f;
```

6.
```javascript
  (function f(){
    function f(){ return 1; }
    return f();
    function f(){ return 2; }
  })();
```

7.
```javascript
  function f(){ return f; }
  new f() instanceof f;
```

8.
```javascript
var count = 0; 
 
var timer = setInterval(function(){ 
  if ( count < 5 ) { 
    console.log( "Timer call: ", count ); 
    count++; 
  } else { 
    clearInterval( timer ); 
  } 
}, 100);
```

9.
```javascript
isC2LSupported: function() {
  if(window.PsNavigate ||
    (window.interOp && window.interOp.postMessage) ||
    (window.webkit && window.webkit.messageHandlers && window.webkit.messageHandlers.interOp && window.webkit.messageHandlers.interOp.postMessage)) {
      return true;
  }
  return false;
}
```
