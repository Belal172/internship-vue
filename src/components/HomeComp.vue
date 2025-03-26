<template>
<h1>This is home component</h1>
<button v-on:click="test()">Click me</button>
<button v-on:dblclick="test2()">Click me</button>
<h2>{{ count }}</h2>
<h2>Two way binding:&nbsp;{{ xyz }}</h2>
<input type="text" v-model="xyz"><br><br>
<input type="text" placeholder="username" v-model="user">
<input type="password" placeholder="password" v-model="password">
<button v-on:click="fetch()">Get values</button>
<p>{{ fetchedData }}</p>
<h2>Technology</h2>

<label><input type="checkbox" v-model="technologies" value="Java"> Java</label>
<label><input type="checkbox" v-model="technologies" value="PHP"> PHP</label>
<label><input type="checkbox" v-model="technologies" value="HTML"> HTML</label>
<label><input type="checkbox" v-model="technologies" value="JS"> JS</label>

<p>Selected Technologies: {{ technologies }}</p>
<h2>Gender</h2>
<label><input type="radio" v-model="gender" value="Male"> Male</label>
<label><input type="radio" v-model="gender" value="Female"> Female</label>
<label><input type="radio" v-model="gender" value="Other"> Other</label>
<p>Selected Gender: {{ gender }}</p>

<h1 v-if="hari">If Hari</h1>
<h1 v-else>else Hari</h1>
<button v-on:click="hari=!hari">Toggle</button>

<h2>for loop</h2>
<ul>
    <li v-for="item in technologies" :key="item"> {{ item }}</li>

</ul>
<br>
<ul>
    <li v-for="item in users" :key="item.email">
        Name is {{ item.name }} and email is {{ item.email }}
    </li>
</ul>
</template>

<script>
export default {
    name: 'HomeComp',
    data() {
        return {
            count: 0,
            xyz: '',
            user: null,
            password: null,
            fetchedData: null,
            technologies: [],
            gender: null,
            hari: false,
            users: [{
                    name: "milan belal",
                    email: "mohitbelal9@gmail.com"

                },
                {
                    name: "ankit belal",
                    email: "ankitbelal@gmail.com"

                },
                {
                    name: "yuvi belal",
                    email: "yuvikachar@gmail.com"

                }
            ]

        }

    },
    methods: {
        test() {
            this.count = this.count + 1
        },
        test2() {
            alert("double clicked")
        },
        fetch() {
            this.fetchedData = {
                user: this.user,
                password: this.password

            }
        }
    }

}
</script>

<style scoped>
h1 {
    color: aqua;
}

h2 {
    color: green;
}
</style>
