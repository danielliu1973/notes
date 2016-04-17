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
(function() {
  return typeof arguments[0]();
})(foo.bar);
```

3.
```javascript
var foo = {
  bar: function() { return this.baz; },
  baz: 1
};
typeof (f = foo.bar)();
```

4.
```javascript
(function(foo) {
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
(function f() {
  function f() { return 1; }
  return f();
  function f() { return 2; }
})();
```

7.
```javascript
function f() { return f; }
new f() instanceof f;
```

8.
```javascript
var count = 0; 
 
var timer = setInterval(function() {
  if (count < 5) { 
    console.log('Timer call: ', count); 
    count++; 
  } else { 
    clearInterval(timer); 
  } 
}, 100);
```

9.
```javascript
function X() {
  this.f = function() {
    return true; 
  }; 
} 
 
// Should return false, but will be overridden 
X.prototype.f = function() {
  return false; 
}; 
 
var x = new X(); 
x.f();
```

10.
```javascript
function X() { }
 
var x1 = new X();
X.prototype.f = function(){ 
  return false; 
}; 

var x2 = new X();
x1.f();
x2.f();
```

11.
```javascript
function foo() {
  this.isLive = true; 
} 
foo(); 
alert(isLive); 
```

12.
```javascript
var obj = { 
  foo: function() {
    this.isLive = true;
  } 
}; 
obj.foo(); 
alert(isLive);
```

13.
```javascript
var obj = {}; 
function foo() { 
  return this; 
} 
alert(foo() == this); 
alert(foo.call(obj) == obj);
```

14.
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
