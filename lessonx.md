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

			angular.element().css()
							 .addClass()
							 .removeClass();
								
			Ext.dom.Element.setStyle()
						   .addCls()
						   .removeCls();
			
	1. box model
		1. [http://www.w3schools.com/css/css_boxmodel.asp](http://www.w3schools.com/css/css_boxmodel.asp)
		1. [https://developer.mozilla.org/en-US/docs/Web/CSS/box_model](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model)
	1. CSS image
		1. background vs img vs content [http://stackoverflow.com/questions/492809/when-to-use-img-vs-css-background-image](http://stackoverflow.com/questions/492809/when-to-use-img-vs-css-background-image)
		1. sprites
		1. replacement (pros & cons)
			1. unicode code [http://unicode-table.com/en/](http://unicode-table.com/en/)
					
					p::after {
					   content: '\2930';
					}

			1. font [http://fortawesome.github.io/Font-Awesome/](http://fortawesome.github.io/Font-Awesome/)
			1. css3

					.arrow-up {
						width: 0; 
						height: 0; 
						border-left: 5px solid transparent;
						border-right: 5px solid transparent;
						
						border-bottom: 5px solid black;
					}
			
				[android logo](https://developer.cdn.mozilla.net/media/uploads/demos/M/d/MdAshrafMalik/e03f62ad7a10045e9b8f6b9243d157ff/css3-android-animate_1412954303_demo_package/index.html)
			
			1. svg [https://css-tricks.com/using-svg/](https://css-tricks.com/using-svg/)
			1. canvas
	1. CSS3 [https://css-tricks.com/snippets/css/](https://css-tricks.com/snippets/css/)
		1. google font [https://css-tricks.com/snippets/css/basics-of-google-font-api/](https://css-tricks.com/snippets/css/basics-of-google-font-api/)
		1. gradients 
			[background](https://css-tricks.com/css3-gradients/)
			[text](https://css-tricks.com/snippets/css/gradient-text/)
		1. border-radius
		1. Animation
		1. Media queries
		1. Many others
