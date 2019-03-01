<template>
    <div>
        <h2 class="signin-heading">Sign In</h2>
        <div class="signin-container">
            <form action="">
                <div>
                    <input type="email" name="" id="" placeholder="Your email.">
                </div>
                <div>
                    <input type="password" name="" id="" placeholder="Your password.">
                </div>
                <div class="signin--btn">
                    <button type="submit">Sign In</button>
                    <a href="#">Forgot your password --></a>
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

.signin-heading {
    text-align: left;
    font-size: 1.2em;
    font-weight: bold;
}

.signin-container {
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
    
    .signin--btn {
        display: flex;
        justify-content: space-between;
        button {
            width: 25%;
            height: 50px;
            font-family: $fontHeader;
            font-weight: 500;
            text-transform: uppercase;
            background-color: transparent;
            border: 2px solid #737373;
            font-size: 16px;
            letter-spacing: 1px;
            cursor: pointer;
            padding: 0;
            &:hover {
                background-color: $linkStates;
                transition: .5s;
                color: $primaryColor;
                border-color: $linkStates;
            }
        }
        p {
            width: 45%;
        }
    }

    input[type="text"], input[type="password"], input[type="email"], input[type="submit"] {
        padding: 5px 5px;
        width: 100%;
    }
}

</style>
