https://frontendmasters.com/live-event/vue/
^ I watched that
https://github.com/sdras/intro-to-vue

I can use vue via webpacker in a rails app

In codepen, put this on top: Vue.config.devtools = true


Directives:
v-text
v-html
v-for      loops through a set of values. Basicallly, a for loop wihich is much cleaner
v-model  creates a relationship between the data in the instance/components and 


Always write data as a function and return it. Because we need to isolate scope.

Modifiers
v-mode.trim will strip any leadiner or trailing whitespace
v-model.number changes strings to number inputs
v-model.lazy  waits until model is bound. Don’t need to show everything.
 
v-if

v-bind (or you can just put “:”)
Binding class and style, lots of things.
v-on  binding events like click. You can also write @ sign instead. 
You can also do multiple binding.

Lots of modifiers 

Methods, Computed, Watchers
Computed properties are calculations that will be cached and not update unless changed.

Computed runs only when a dependency changed
Computed is cached
Computed should be used as a property, in place of data
Copmuted by default getter only, but you can define a setter
Methods run whenever an update occurs
Methods not cached
Methods typically invoked from v-on/@. but flexible

What is reactive programming? Programming with asynchronous data streams.
A stream is a sequence of ongoing events ordered in time that offer some hooks with which to observe it.
This means it’s very easy to update state in reaction to events.

(read Andre Staltz’ blog post)

Vue uses getters/setters for this.


Templates: Vue uses HTML-based template syntax to bind the Vue instance to the DOM, very useful for components.
Templates for optional, you can also write render functions. 
Use strings for simple cases. Then you can use script. Or go with single file templates.

Components: a collection of elements that are encapsulated into a group that can be accessed through one single element.



html
js
<div id="app">
  <child></child>
</div>



Vue.config.devtools = true

Vue.component('child', {
  template: `<div>Hello there</div>`
});

new Vue({
  el: "#app"
});





If you want to re-use a component, but want it to output somethign different (usually a small thing), that’s why you would use props.


html
js

<div id="app">
  <child :text="message"></child>
</div>




Vue.config.devtools = true

Vue.component('child', {
  props: ['text'],
  template: `<div>{{ text }}</div>`
});

new Vue({
  el: "#app",
  data() {
    return {
      message: 'hello mr. magoo'
    }
  }
});





:text = v-bind:text

Props - passing data down from the parent to the child.
Props - you can think of it a little like the component holds a variable that is waiting to be filled out by whatever the parent sends down to it.

Props: types and validation
You can have a default too. But always write it as a function:


text: {
type: Object,
default: function () {
    return { message: ‘hello mr. magoo’ }
    }
}

You can create local components if all your code is in one file (const individualComment =). But have to use “Vue.component” if you are separating code.

Communicating Events

