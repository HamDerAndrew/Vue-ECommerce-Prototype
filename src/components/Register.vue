<template>
    <div>
        <h2 class="register-heading">Register</h2>
        <div class="register-container">
            <form action="" novalidate="true">
                  <p v-if="errors.length">
                    <b>Please correct the following error(s):</b>
                    <ul>
                    <li v-for="error in errors" :key="error">{{ error }}</li>
                    </ul>
                </p>
                <div>
                    <input type="email" name="email" id="email" v-model="email" placeholder="Email.">
                </div>
                <div>
                   <input type="password" name="password" id="" v-model="password" placeholder="Password.">
                </div>
                <div>
                    <input type="password" name="confirmpassword" id="" placeholder="Confirm password.">
                </div>
                <div class="checkbox--btn">
                    <input type="checkbox" name="" id="">
                    <p>Sign up for exclusive updates, discounts, new arrivals, contests, and more!</p>
                </div>
                <div class="register--btn">
                    <button v-on:click="checkForm" type="submit">Create Account</button>
                    <p>By clicking 'Create Account', you agree to our <a href="#">Privacy Policy</a></p>
                </div>
                
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            errors:[],
            email:null,
            password:null
        };
    },
    methods:{
    checkForm:function(e) {
        this.errors = [];
        if(!this.password) this.errors.push("Password required.");
        if(!this.email) {
            this.errors.push("Email required.");
        } else if(!this.validEmail(this.email)) {
            this.errors.push("Valid email required.");        
        }
        if(!this.errors.length) return true;
        e.preventDefault();
        }
    }
}
</script>

<style lang="scss">
@import "@/scss/_var.scss";
@import "@/scss/_mixins.scss";

.register-heading {
    text-align: left;
    font-size: 1.2em;
    font-weight: bold;
}

.register-container {
    color: $paragraphColor;
    text-align: left;

    p {
        font-size: 12px;
    }
    
    div {
        margin: 20px auto;
        width: 100%;
    }

    a {
        color: $linkStates;
    }

    .checkbox--btn {
        display: flex;
        flex-wrap: no-wrap;
        align-items: baseline;
    }
    
    .register--btn {
        display: flex;
        justify-content: space-between;
        button {
            width: 40%;
            @include ctaButton;
        }
        p {
            width: 40%;
        }
    }

    input[type="text"], input[type="password"], input[type="email"], input[type="submit"] {
        padding: 5px 5px;
        width: 100%;
        border: 1px solid #80808040;
    }
    input[type="checkbox"] {
        border-radius: 0;
        margin: 0 5px 0 0;
    }
}

</style>
