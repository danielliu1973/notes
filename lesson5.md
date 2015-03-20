#Go over
1. Javascript
1. Class system
1. Component, Container, Layout
1. ComponentQuery
1. Event
#New
1. SenchaMVC

		Ext.application({
			requires: ['Ext.container.Viewport'],
			name: 'Homework',

			appFolder: 'app',

			launch: function() {
				Ext.create('Ext.container.Viewport', {
					layout: 'fit',
					items: [{
						xtype: 'panel',
						title: 'Users',
						items : []
					}]
				});
			}
		});



		Ext.Loader.setPath('Homework', 'app');

		Ext.require([
			'Ext.container.Viewport',
			'Ext.tab.Panel',
			'Homework.view.FundPanel',
			'Homework.view.EmployeeAdminPanel',
		]);

		Ext.onReady(function() {
			Ext.create('Ext.container.Viewport', {
				layout: 'fit',

				items: [{
					xtype: 'tabpanel',
					activeTab: 2,
					items: [{
						xtype: 'fundpanel'
					}, {
						xtype: 'employeeadminpanel'
					}, {
						xtype: 'panel',
						title: 'Contact Window',
						items: [{
							xtype: 'button',
							text: 'click',
							handler: function() {
								Ext.create('Homework.view.ContactWindow').show();
							}
						}]
					}]
				}]

			});
		});