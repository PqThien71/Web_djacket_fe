<template>
    <div class="page-login">
        <h1>Login</h1>
        <form @submit.prevent="submitForm">
            <div class="field">
                <label>UserName</label>
                <div class="control">
                    <input type="text" class="input" v-model="username">
                </div>
            </div>
            <div class="field">
                <label>Password</label>
                <div class="control">
                    <input type="password" class="input" v-model="password">
                </div>
            </div>        
            <div class="notification is-danger" v-if="errors.length">
                <p v-for="error in errors" v-bind:key="error">{{ error }}</p>
            </div>

            <div class="field">
                <div class="control">
                    <button class="button is-dark"> SignUp </button>
                </div>
            </div>
            <hr>
            Or <router-link to="/log-in" >Click here</router-link> to login
        </form>
    </div>
</template>
<script>
export default{
    name: 'Login',
    data(){
        return
    },
}
</script>