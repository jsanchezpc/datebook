<template>
    <div id="signin-body">
        <div class="row-signin" id="signup">
            <SignUpComponent class="log-box" />
        </div>
        <div class="row-signin" id="login">
            <LogInComponent class="log-box" />
        </div>
    </div>
</template>
  
<script>
import LogInComponent from "../components/LogInComponent.vue";
import SignUpComponent from "../components/SignUpComponent.vue";

export default {
    name: "SignInView",
    components: {
        LogInComponent,
        SignUpComponent,
    }
};
</script>
  
<style lang="scss" scoped>
div#signin-body {
    overflow-x: hidden;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 100%;
    height: 100lvh;
    background-color: rgb(200, 203, 221);

    div.row-signin {
        flex: 50%;
    }

    @media screen and (max-width: 1070px) {
        div.row-signin {
            flex: 100%;
        }
    }

    div.log-box {
        background-color: black;
        width: 100%;
        height: 100lvh;
        color: white;
        display: block;
        margin: auto;
        padding: 10px;
    }
}
</style>
  