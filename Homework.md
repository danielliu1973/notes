1. implement function add(a, b, c...)
  ```javascript
    add(3); // returns 3
    add(3, 4);  // returns 7
    add(3, 4, 5);  // returns 12
  ```

1. impplement function max(a, b, c...)
  ```javascript
    max(3); // returns 3
    max(3, 4);  // returns 4
    max(3, 4, 5);  // returns 5
  ```

1. implement function clone

1. You have the following JavaScript code. Write the appropriate HTML so all three statements are equivalent (will bring the same value).

  ```javascript
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

  ```javascript
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
  ```javascript
	sum(3)(4); // returns 7
	```

1. Tell me what the function below does. Do you see the bug?
  ```javascript
	function foo(arr) {
		var a1 = -Infinity, a2 = -Infinity;
		arr.forEach(function(num) {
			if (num > Math.min(a1, a2)) {
				if (a1 < a2) {
					a1 = num;
				} else {
					a2 = num;
				}
			}
		});
		return (Math.min(a1, a2));
	}
	```

1. Highlights in resume
1. Explain what is MVC
1. Do the quiz. [http://www.w3schools.com/quiztest/quiztest.asp?qtest=JavaScript](http://www.w3schools.com/quiztest/quiztest.asp?qtest=JavaScript)
1. Implement the screenshot below using ExtJS
	* [screen1.png](img/screen1.png)
	* [screen2.png](img/screen2.png)
