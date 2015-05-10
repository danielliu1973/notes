#Go over
1. Typescript

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

1. CSS
	1. Style

			<div style="font-size: 10px;"></div>
	
	1. Seletor	
		1. simple selector, id, class, tag, attribute
				
				<span id="id">select by id<.span>
				#id {...}

				<span class="clsName">select by class</span>
				clsName {...}

				<div>select by tag</div>
				div {...}

				<div attr="attr">select by attribute</div>
				[attr] {...}
		
		1. universal

				* {...}
		
		1. combinateion

				<!-- select by group -->
				<div>test div</div>
				<span>test span</span>
				div, span {...}

				<!-- select by direct child -->
				<li>
					<button>click me</button>
				</li>
				li>button {...}
				
				<!-- select by descendant -->
				<li>
					<div>
						<button>click me</button>
					</div>
				</li>
				li button {...}
				
				<!-- select by sibling -->
				<div></div>
				<span></span>
				div+span {...}
	
		1. pseudo class

				a:link, a:visted, a:hover, a:active
				button:hover
				:first-child, :last-child
				
				:nth-child(), :nth-last-child(), :only-child
				:not()
				:enabled, :disabled, :checked
				
		1. pseudo element

				::after
				::before
				::first-letter
				::first-line
				::selection
	
	1. Javascript
			
			element.querySelector('div.clsName');
			element.querySelectorAll('div,span');
	
	1. box model
	1. CSS3
		1. CSS image sprites
		1. Gradients
		1. Transforms
https://css-tricks.com/snippets/css/css-triangle/