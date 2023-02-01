First Steps in Vue JS

# RandomUser

Simple Vue JS application using CDN

1. Create files - index.html, style.css, app.js
2. Add CDN script in body tag
```
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script> 
```
3. Create your app variable in js and mount it.
```
const app = Vue.createApp({
    template: '<h1>Hello World</h1>'
})
app.mount('#app')
```
4. To use data - create a function and it should return the object
```
const app = Vue.createApp({
    template: '<h1>Hello {{firstName}}</h1>',
    data(){
        return {
            firstName: 'John'
        }
    }
})
```
* V-BIND --> v-bind:src, v-bind:alt, v-bind:class
* V-ON --> v-on:click
