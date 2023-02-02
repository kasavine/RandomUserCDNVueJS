# Random User

This project is a simple Vue.js application that fetches a random user from an API (randomuser.me/api) and displays the user's information on the screen.

### Project Setup - CDN
This is simple one page app, you don't need to install anything.
Clone the project and run index.html

### Built With
* Vue.js
* CSS (styling)

![Alt Text](random_user.gif)

### Notes

1. **Generate** the following files: index.html, style.css, app.js

2. Include both the **CDN script** and the **app script** within the body tag.
```
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script> 
<script src="app.js"></script>
```

3. Declare an app variable in your JavaScript file and mount it.
```
const app = Vue.createApp({
    ...
})
app.mount('#app')
```

4. To access data, create a function that returns an object.
```
const app = Vue.createApp({
    data(){
        return {
            firstName: 'First',
            lastName: 'Last',
            email: 'first.last@gmail.com',
            gender: 'female',
            picture: 'https://randomuser.me/api/portraits/women/10.jpg'
        }
    }
})
```

5. Include a method called "getUser()" in your app and use it to retrieve data.
```
methods: {
        async getUser(){
            const res = await fetch("https://randomuser.me/api");
            const {results} = await res.json();
            this.firstName = results[0].name.first;
            this.lastName = results[0].name.last;
            this.email = results[0].email;
            this.gender = results[0].gender;
            this.picture = results[0].picture.large;
        }
    }
```