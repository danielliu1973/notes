# Go over
1. Closure
1. ExtJS
    1. Sencha Command
    1. UI components
        1. Element & Container
        1. Layouts
# New

1. Ext.Component
    1. config
        1. id, itemId
        1. margin, padding
        1. width, height, minWidth, minHeight, maxWidth, maxHeight
        1. autoScroll
        1. cls, style, baseCls
        1. border, frame
        1. hidden, hideMode
        1. disabled, disabledCls
        1. autoEl
        1. tpl
        1. stateful, stateId
    1. method
        1. disable(), enable()
1. Form fields
    1. config
        1. name
        1. fieldLabel, fieldStyle, fieldCls
        1. labelWidth, labelAlign, labelCls, labelStyle, labelSeparator
        1. hideEmptyLabel, hideLabel
        1. readOnly, readOnlyCls, disabled, disabledCls, emptyCls, emptyText, dirtyCls
        1. originalValue, isDirty(), dirtyCls
        1. enforceMaxLength
        1. enableKeyEvents
        1. submitValue
        1. formBind
        1. Validation text & class
            1. vtype
            1. validator
            1. allowBlank
            1. msgTarget
            1. blankText, invalidText, invalidCls
    1. methods
        1. getValue(), getRawValue()
        1. getActiveErrors(), setActiveErrors(), getErrors(), markInvalid()
        1. isValid(), clearInvalid()
        1. checkChange(), checkDirty(), isDirty(), resetOriginalValue()
        1. rawToValue(), valueToRaw()
1. Containers: container, panel, window, form, tab, fieldset, fieldcontainer
    1. config
        1. bubbleEvents
        1. defaults, defaultType
        1. items
        1. layout
    1. method
        1. add(), remove(), removeAll
        1. child(), down()
1. Form
    1. method
        1. getValues()
        1. isDirty(), isValid()
        1. load(), submit(), loadRecord(), getRecord()
        1. getForm()
    1. Basic
        1. getFieldValues(), getValues()
        1. findField(), getFields()
        1. isDirty(), isValid()
        1. checkDirty(), checkValidity(), clearInvalid(), markInvalid()
        1. load(), submit(), loadRecord(), getRecord(), setValues()
1. Data Package
    1. Ext.data.Store
        1. fields: name, type
        1. model
        1. each(), getAt()
        1. getCount(), getTotalCount()
    1. Ext.data.Model
        1. fields, idProperty
        1. get()
        1. isModified()
        1. commit(), reject()
        1. validations
        1. validate(), isValid(), dirty
    1. Ext.data.proxy.Proxy
        1. url
        1. api
        1. timeout: global setting
        1. extraParams
        1. limitParam, pageParam etc.
        1. reader
    1. Ext.data.reader.Json
        1. successProperty, totalProperty, root
    1. Sample

            me.store = new Ext.data.Store({
	    		proxy: {
		    		type: 'ajax',
			    	url: 'path/getUserAccountBalances',
				    extraParams: {
					    userId: me.getUserId()
    				},
	    			reader: {
		    			type: 'json',
			    		root: 'items'
				    }
    			},
	    		fields: [
		    		{name: 'CURRENCY'},
			    	{name: 'CURRENCYBALANCE', type : 'float'},
				    {name: 'DEFAULT', type: 'boolean'}
    			],
	    		listeners: {
		    		load: function(s, records, success) {
					    
			    	}
    			}
	    	});

1. Grid
    1. column
        1. text, dataIndex, renderer
    1. viewConfig
        1. trackOver, enableTextSelection, markDirty, stripeRows
1. ComboBox
    1. store
    1. listConfig
        1. width, height, minWidth, maxWidth, minHeight, maxHeight
        1. itemSelector, getInnerTpl
1. View
1. Tree/Time
1. Events
1. Component Query
    1. CSS selector
        1. [http://www.w3schools.com/cssref/css_selectors.asp](http://www.w3schools.com/cssref/css_selectors.asp)
        1. [https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors)
        1. [http://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048](http://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048)
    1. performance
1. SenchaMVC
1. resources
    1. [http://www.sencha.com/blog/top-10-ext-js-development-practices-to-avoid/](http://www.sencha.com/blog/top-10-ext-js-development-practices-to-avoid/)