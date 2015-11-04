1. prototype
    1. prerequisite  
        pointer, reference
    1. prototype vs \__proto__

        ···javascript
        function Person(name) {
            this.name = name;
        }
        Person.prototype.getName = function() {
            return this.name;
        };
        var person = new Person('Aaron');
        var person = {};
        Person.call(person, 'Aaron');
        person.__proto__ = Person.prototype;
        var p2 = new Person('Ding');
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

        function Student(name, id) {
            Person.call(this, name);
            this.id = id;
        }

        __extends(Student, Person);

        Student.prototype.getId = function() {
            return this.id;
        };
        ```
    
    1. prototype chain (\_\_proto\_\_ chain)

        ```javascript
        var p = new Person();
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
        1. [Object.create](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Object/create)

1. ExtJS
    
    1. UI components
        1. Element & Container
        1. Layouts
            1. absolute, table
            1. fit, border, accordion, card
            1. auto, anchor, form, vbox
            1. hbox, column
    
