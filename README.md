# vue
vue tutorail

#Hello Vue Js
```html
<!DOCTYPE html>
<html>

<head>
    <title>Hello Vue Js</title>
    <script src="vue.js"></script>
</head>

<body>
    <div id="app">
        {{ message }}
    </div>

    <script type="text/javascript">
    var app = new Vue({
        el: '#app',
        data: {
            message: 'Hello Vue Js!'
        }
    });
    </script>
    
</body>

</html>


```

##computed:
Computed properties to be mixed into the Vue instance.Computed properties are cached, and only re-computed on reactive dependency changes. Computed properties are by default getter-only, but you can also provide a setter when you need it:
```js
// ...
computed: {
  fullName: {
    // getter
    get: function () {
      return this.firstName + ' ' + this.lastName
    },
    // setter
    set: function (newValue) {
      var names = newValue.split(' ')
      this.firstName = names[0]
      this.lastName = names[names.length - 1]
    }
  }
}
// ...
```

##methods
Methods to be mixed into the Vue instance. You can access these methods directly on the VM instance, or use them in directive expressions.

##watch
An object where keys are expressions to watch and values are the corresponding callbacks. 

#computed Vs methods
the two approaches are indeed exactly the same. However, the difference is that **computed properties are cached based on their dependencies**. A computed property will only re-evaluate when some of its dependencies have changed.

##computed Vs watched
Vue does provide a more generic way to observe and react to data changes on a Vue instance: **watch properties.** While computed properties are more appropriate in most cases, there are times when a custom watcher is necessary. That’s why Vue provides a more generic way to react to data changes through the watch option. This is most useful when you want to perform asynchronous or expensive operations in response to changing data.



