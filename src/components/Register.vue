<template>
    <div>
        <h2 class="register-heading">Register</h2>
        <div class="register-container">
            <form action="">
                <div>
                    <input type="email" name="" id="" placeholder="Your email.">
                </div>
                <div>
                    <input type="password" name="" id="" placeholder="Your password.">
                </div>
                <div>
                    <input type="password" name="" id="" placeholder="Confirm password.">
                </div>
                <div class="checkbox--btn">
                    <input type="checkbox" name="" id="">
                    <p>Sign up for exclusive updates, discounts, new arrivals, contests, and more!</p>
                </div>
                <div class="register--btn">
                    <button type="submit">Create Account</button>
                    <p>By clicking 'Create Account', you agree to our <a href="#">Privacy Policy</a></p>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "@/scss/_var.scss";

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
            font-family: $fontHeader;
            font-weight: 500;
            text-transform: uppercase;
            background-color: transparent;
            border: 2px solid #737373;
            font-size: 13px;
            letter-spacing: 1px;
            cursor: pointer;
            padding: 5px 10px;
            &:hover {
                background-color: $linkStates;
                transition: .5s;
                color: $primaryColor;
                border-color: $linkStates;
            }
        }
        p {
            width: 40%;
        }
    }

    input[type="text"], input[type="password"], input[type="email"], input[type="submit"] {
        padding: 5px 5px;
        width: 100%;
    }
    input[type="checkbox"] {
        border-radius: 0;
        margin: 0 5px 0 0;
    }
}

</style>
