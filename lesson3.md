1. prototype
    1. prerequisite  
        pointer, reference
    1. prototype vs \__proto__

        ```javascript
        function Person(name, age) {
            this.name = name;
            this.age = age;
        }
        Person.prototype.getName = function() {
            return this.name;
        };
        Person.prototype.getAge = function() {
            return this.age;
        };
        var person = new Person('Aaron', 18);
        var person = {};
        Person.call(person, 'Aaron', 18);
        person.__proto__ = Person.prototype;
        var p2 = new Person('Ding', 20);
        ```
        
    1. inheritance

        ```javascript
        var __extends = function (child, parent) {
            for (var p in parent) {
                if (parent.hasOwnProperty(p)) child[p] = parent[p];
            }
            function __() { this.constructor = child; }
            __.prototype = parent.prototype;
            child.prototype = new __();
            //child.prototype = Object.create(parent.prototype);
            //child.prototype.constructor = child;
        };

        function Student(name, age, id) {
            Person.call(this, name, age);
            this.id = id;
        }

        __extends(Student, Person);

        Student.prototype.getId = function() {
            return this.id;
        };
        ```
    
    1. prototype chain (\_\_proto\_\_ chain)

        ```javascript
        var p = new Person('Tom', 15);
        p.getName = function() {/*...*/};
        p.getName();
        ```

    1. instanceof  
        Object.getPrototypeOf(obj) -> obj.\_\_proto\_\_  
        obj instanceof Clazz -> obj.\_\_proto\_\_ === Clazz.prototype || obj.\_\_proto\_\_.\_\_proto\_\_ === Clazz.prototype

        ```javascript
        var o = {};
        console.log(o instanceof Person);
        console.log(o instanceof Student);
        o.__proto__ = Student.prototype;
        ```

    1. Resources  
        1. [http://www.w3schools.com/js/js_object_prototypes.asp](http://www.w3schools.com/js/js_object_prototypes.asp)
        1. [http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/](http://javascriptissexy.com/javascript-prototype-in-plain-detailed-language/)
        1. [http://www.crockford.com/javascript/inheritance.html](http://www.crockford.com/javascript/inheritance.html)
        1. [http://javascript.crockford.com/prototypal.html](http://javascript.crockford.com/prototypal.html)
        1. [http://openwares.net/js/javascript_prototype_chain.html](http://openwares.net/js/javascript_prototype_chain.html)
        1. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/prototype](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/prototype)
        1. [http://ms.csdn.net/share/2F555591FBA7ACD734AA8882189441D6_1_IPHONE_APP](http://ms.csdn.net/share/2F555591FBA7ACD734AA8882189441D6_1_IPHONE_APP)
        1. [Object.create](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/create)

1. ExtJS introduction
    1. smartclient, kendo ui
    1. Real examples
        1. [synology](https://www.synology.com/en-us/dsm/5.2/live_demo)
        1. [sitescout](https://rtb.sitescout.com/)
    1. History
    1. Development mode & production mode
    1. Sencha Command
	1. Examples:
		1. Forms, ComboBox, Grids, Windows, Layout Managers, Toolbars and Menus
		1. DataView
		1. Tabs, Trees
		1. Drag & Drop
		
1. ExtJS interview questions
    1. [http://www.withoutbook.com/Technology.php?tech=65&subject=ExtJS%20Interview%20Questions%20and%20Answers](http://www.withoutbook.com/Technology.php?tech=65&subject=ExtJS%20Interview%20Questions%20and%20Answers)
    1. [http://atoz-tech.blogspot.ca/2011/07/extjs-interview-questions.html](http://atoz-tech.blogspot.ca/2011/07/extjs-interview-questions.html)
    1. [http://interviewquestionsanswers.org/forum/topic-1553-65-ext-js-interview-questions-and-answers-page-1.html](http://interviewquestionsanswers.org/forum/topic-1553-65-ext-js-interview-questions-and-answers-page-1.html)
    1. [http://www.globalguideline.com/interview_questions/Questions.php?sc=Ext_JS](http://www.globalguideline.com/interview_questions/Questions.php?sc=Ext_JS)
    1. [http://sureshat25.blogspot.ca/2014/12/ext-js-interview-question-and-answers.html](http://sureshat25.blogspot.ca/2014/12/ext-js-interview-question-and-answers.html)
    1. [http://extjsexamples.blogspot.ca/2013/05/extjs4-interview-questions-answers.html](http://extjsexamples.blogspot.ca/2013/05/extjs4-interview-questions-answers.html)

1. ExtJS development
	1. Class system
    1. [http://www.extjs-tutorial.com/extjs/naming-convention](http://www.extjs-tutorial.com/extjs/naming-convention)
    1. UI components
        1. Element & Container
        1. Layouts
    1. Layout system
        1. absolute, table
        1. fit, border, accordion, card
        1. auto, anchor, form, vbox
        1. hbox, column
    1. Store, Model, Proxy, View
    1. Events
1. ExtJS dev rules
    1. no id
    1. no global functions
    1. no functions in strings
    
