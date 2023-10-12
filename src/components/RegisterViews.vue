<template>
    <div class="registration">
        <h3>Register here</h3>
        <hr>
        <div class="row" v-for="user in users">
            <h4> {{ user.name }}</h4>
            <button @click="registerUser(user)">Register</button>
        </div>
    </div>
</template>

<script>
export default {
    props: ['users'],
    methods: {
        registerUser(user) {
            this.$emit('userRegistred', user);
            user.registred = true;
        }
    },
}
</script>