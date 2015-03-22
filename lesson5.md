#Go over
1. Javascript
1. Class system
1. Component, Container, Layout
1. ComponentQuery
1. Event
#New
1. SenchaMVC
	1. application

			Ext.application({
				name: 'Homework',
				appFolder: 'app',
				requires: [
					...
				],

				launch: function() {
					Ext.create('Ext.container.Viewport', {
						layout: 'fit',
						items: [{
							...
						}]
					});
				}
			});

		vs

			Ext.Loader.setPath('Homework', 'app');

			Ext.require([
				...
			]);

			Ext.onReady(function() {
				Ext.create('Ext.container.Viewport', {
					layout: 'fit',
					items: [{
						...
					}]
				});
			});

	1. controller
		1. refs
		1. models, views, stores
		1. init(), control()

1. Advanced ExtJS
	1. Form validation
	1. View
	1. Custom control
	1. DOM