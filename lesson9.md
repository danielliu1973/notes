#Go over
1. deferred promise pattern
1. Factory, Service
1. Directives
1. Filters

#New
1. Events
	1. DOM event [http://www.w3schools.com/jsref/dom_obj_event.asp](http://www.w3schools.com/jsref/dom_obj_event.asp)

			document.addEventListener('myevent', function() {
  				console.log('received 1');
			});

			document.addEventListener('myevent', function() {
  				console.log('received 2');
			});
			
			document.dispatchEvent(new Event('myevent'));
			
	1. AngularJS event [https://docs.angularjs.org/guide/scope](https://docs.angularjs.org/guide/scope)

			angular.module('eventExample', [])
			.controller('EventController', ['$scope', function($scope) {
			  $scope.count = 0;
			  $scope.$on('MyEvent', function() {
			    $scope.count++;
			  });
			  
			  //$emit('MyEvent');
      		  //$broadcast('MyEvent');
			}]);
	1. ExtJS event
		1. Ext.util.Observable
		1. enableBubble
		1. addListener, addManagedListener, on, mon
		1. fireEvent

1. [Typescript](http://www.typescriptlang.org/)
	1. compile to javascript languages
		1. CoffeeScript
		1. GWT
		1. Dart
		1. Many others
	1. Advantages
		1. Backed by Microsoft
		1. Developed by [Anders Hejlsberg](http://en.wikipedia.org/wiki/Anders_Hejlsberg)
		1. Superset of Javascript (use existing librarys)
		1. ECMAScript 6 standard (forward compatiblity)
		1. Relation with AngularJS
		1. Debugging
1. Install
	1. Node.js
	1. npm install -g typescript
1. Features
	1. types: number, string, boolean, Array, Enum, Void, function, any

			var num: number = 1;
			var str: string = 'string';
			var bool: boolean = false;
			var arr: Array<string> = ['abc', 'ddd'];
			enum Day {SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY};
			var day: Day = Day.MONDAY;
			var func: (a:number, b:number)=>number;
			function add(left: number, right: number): number {
				return left + right;
			}
			func = add;
			var any: any = 3;
			any = 'foo';

	1. interface
