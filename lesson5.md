#Go over
1. Javascript
1. Class system
1. Component, Container, Layout
1. ComponentQuery
1. Event
#New
1. SenchaMVC

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
						xtype: 'panel',
						title: 'Users',
						items : [
							...
						]
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