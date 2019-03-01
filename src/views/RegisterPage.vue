<template>
    <div class="register">
        <intro-header-app :boldHead="spanEl" :heading="heading" :subInfo="subInfo"></intro-header-app>
        <div class="account-page">
            <div class="account-signin">
                <sign-in-app></sign-in-app>
            </div>
            <span class="vertical-line"></span>
            <div class="account-register">
                <register-app></register-app>
            </div>
        </div>
    </div>
</template>

<script>
import HeaderIntro from '../components/HeaderIntro.vue';
import Register from '../components/Register.vue';
import SignIn from '../components/SignIn.vue';

export default {
    name: 'register',
    components: {
        "intro-header-app": HeaderIntro,
        "register-app": Register,
        "sign-in-app": SignIn

    },
    data() {
        return {
            spanEl: "Welcome",
            heading: "to ave",
            subInfo: "Sign in or register"
        };
    }
}
</script>

<style>

</style>
