1. You have the following JavaScript code. Write the appropriate HTML so all three statements are equivalent (will bring the same value).

```
	document.forms["myForm"].elements["myField"].value
	document.forms[1].elements[1].value
	document.myForm.myField.value
```

1. Read the API on object String and Array.
	[http://docs.sencha.com/extjs/4.2.1/#!/api/String](http://docs.sencha.com/extjs/4.2.1/#!/api/String)
	[http://docs.sencha.com/extjs/4.2.1/#!/api/Array](http://docs.sencha.com/extjs/4.2.1/#!/api/Array)

	Then write a one-line function (less than 80 characters) that returns a boolean indicating whether or not a string is a palindrome. e.g. "A nut for a jar of tuna." is a palindrome.

1. Read this article then run the following code in a browser and explain the result. 

	[http://ryanmorr.com/understanding-scope-and-context-in-javascript/](http://ryanmorr.com/understanding-scope-and-context-in-javascript/)

```
	var myObject = {
		foo: "bar",
		func: function() {
			var self = this;
			console.log("outer func:  this.foo = " + this.foo);
			console.log("outer func:  self.foo = " + self.foo);
			(function() {
				console.log("inner func:  this.foo = " + this.foo);
				console.log("inner func:  self.foo = " + self.foo);
			})();
		}
	};
	myObject.func();
	var test = myObject.func;
	test();
	```

1. Implement the following function. It should return the sum of the two numbers:

    sum(3)(4); // returns 7
	
1. Tell me what the function below does. Do you see the bug?
```
	function foo(arr) {
		var max1 = -Infinity, max2 = -Infinity;
		arr.forEach(function(num) {
			if (num > Math.min(max1, max2)) {
				if (max1 < max2) {
					max1 = num;
				} else {
					max2 = num;
				}
			}
		});
		return (Math.min(max1, max2));
	}
```