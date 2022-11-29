<template>
    <div>
        <h1>Registration form</h1>
    <form @submit="submit">
    
        <label>Name: </label>
        <input type="text" v-model="name" placeholder="Enter your name">
        <br><br>
    
        <label>Email: </label>
        <input type="email" v-model="email" placeholder="Enter your email id">
        <br><br>
    
        <label>Address: </label>
        <input type="text" v-model="address"><br><br>
    
        <fieldset>
                    <legend align="center">Select your gender</legend>
                    <input type="radio" name="gender" value="male" id="m"> <label for="m">Male</label><br>
                    <input type="radio" name="gender" value="female" id="f"><label for="f">Female</label><br>
                    <input type="radio" name="gender" value="other" id="o"><label for="o">Other</label><br>
            </fieldset><br>
    
        <label>Password: </label>
        <input type="password" v-model="password" placeholder="Enter password">
        <br><br>
    
        <button type="button" @click= "submit"> Submit </button>
    
        <div v-if= "Submit">
            <h3> Form submitted </h3>
            <p> Name: {{ name }} </p>
            <p> Email: {{ email }} </p>
            <p> Address: {{address}} </p>
            <p> Gender: {{gender}} </p>
            <p> Password: {{password}} </p>
        </div>
    </form>
    </div>
    
    </template>
    
    <script>
    export default {
        name: 'app',
        data() {
            return {
                name: '',
                email: '',
                address: '',
                gender: '',
                password: '',
                Submit: false
            };
        },
        methods: {
            submit() {
                this.Submit = true
            }
        },
    };
    </script>