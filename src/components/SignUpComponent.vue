<template>
    <div id="signup-body">
        <h1 class="sign-title">OPEN YOUR DATEBOOK TODAY</h1>
        <div v-if="screenWidth <= 1070"
            style="width: 60%; display: flex; flex-direction: column; margin: auto;text-align: right;">
            <a style="text-decoration: none;color:black" id="login-link" href="#login">Already have an account?</a>
        </div>
        <br>
        <form @submit="signUp">
            <input class="log-input" required placeholder="Username" type="text" name="username"
                v-model="userInput.username">
            <input class="log-input" required placeholder="Your email" type="email" name="email" v-model="userInput.email">
            <input class="log-input" required placeholder="Password" type="password" name="password"
                v-model="userInput.password">
            <input class="log-input" required placeholder="Repeat your password" type="password" name="repeatPassword"
                v-model="userInput.repeatPassword">
            <div style="width: 60%; display: flex; flex-direction: column; margin: auto;text-align: justify;">
                <label style="cursor: pointer;" for="conditions-box" id="conditions">
                    <input required type="checkbox" name="conditions" id="conditions-box">
                    By checking this box, I acknowledge that I have read, understood, and agreed to abide by the terms and
                    conditions.
                </label>
                <br>
                <br>
                <input id="register-btn" type="submit" value="SEND">
            </div>
        </form>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'SignUpComponent',
    data() {
        return {
            screenWidth: window.innerWidth,
            API_URL: "localhost:8083",
            END_POINT: "/signup",
            userInput: {
                username: '',
                email: '',
                password: '',
                repeatPassword: ''
            }
        }
    },
    methods: {
        signUp() {
            axios.post(this.API_URL + this.END_POINT, this.userInput)
                .then(response => {
                    // Aquí puedes manejar la respuesta exitosa de la API
                    console.log(response.data);
                })
                .catch(error => {
                    // Aquí puedes manejar el error de la API
                    console.error(error);
                });
        }
    }

}
</script>

<style lang="scss" scoped>
div#signup-body {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    background-color: #ff0000;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100%25' height='100%25' viewBox='0 0 1200 800'%3E%3Cdefs%3E%3ClinearGradient id='a' gradientUnits='userSpaceOnUse' x1='600' y1='25' x2='600' y2='777'%3E%3Cstop offset='0' stop-color='%23ff0000'/%3E%3Cstop offset='1' stop-color='%23E0F'/%3E%3C/linearGradient%3E%3ClinearGradient id='b' gradientUnits='userSpaceOnUse' x1='650' y1='25' x2='650' y2='777'%3E%3Cstop offset='0' stop-color='%23fd0017'/%3E%3Cstop offset='1' stop-color='%23d800f3'/%3E%3C/linearGradient%3E%3ClinearGradient id='c' gradientUnits='userSpaceOnUse' x1='700' y1='25' x2='700' y2='777'%3E%3Cstop offset='0' stop-color='%23fc002e'/%3E%3Cstop offset='1' stop-color='%23c300e6'/%3E%3C/linearGradient%3E%3ClinearGradient id='d' gradientUnits='userSpaceOnUse' x1='750' y1='25' x2='750' y2='777'%3E%3Cstop offset='0' stop-color='%23fa0046'/%3E%3Cstop offset='1' stop-color='%23ad00da'/%3E%3C/linearGradient%3E%3ClinearGradient id='e' gradientUnits='userSpaceOnUse' x1='800' y1='25' x2='800' y2='777'%3E%3Cstop offset='0' stop-color='%23f9005d'/%3E%3Cstop offset='1' stop-color='%239700ce'/%3E%3C/linearGradient%3E%3ClinearGradient id='f' gradientUnits='userSpaceOnUse' x1='850' y1='25' x2='850' y2='777'%3E%3Cstop offset='0' stop-color='%23f70074'/%3E%3Cstop offset='1' stop-color='%238200c1'/%3E%3C/linearGradient%3E%3ClinearGradient id='g' gradientUnits='userSpaceOnUse' x1='900' y1='25' x2='900' y2='777'%3E%3Cstop offset='0' stop-color='%23f6008b'/%3E%3Cstop offset='1' stop-color='%236c00b5'/%3E%3C/linearGradient%3E%3ClinearGradient id='h' gradientUnits='userSpaceOnUse' x1='950' y1='25' x2='950' y2='777'%3E%3Cstop offset='0' stop-color='%23f400a2'/%3E%3Cstop offset='1' stop-color='%235700a8'/%3E%3C/linearGradient%3E%3ClinearGradient id='i' gradientUnits='userSpaceOnUse' x1='1000' y1='25' x2='1000' y2='777'%3E%3Cstop offset='0' stop-color='%23f300b9'/%3E%3Cstop offset='1' stop-color='%2341009c'/%3E%3C/linearGradient%3E%3ClinearGradient id='j' gradientUnits='userSpaceOnUse' x1='1050' y1='25' x2='1050' y2='777'%3E%3Cstop offset='0' stop-color='%23f100d1'/%3E%3Cstop offset='1' stop-color='%232b0090'/%3E%3C/linearGradient%3E%3ClinearGradient id='k' gradientUnits='userSpaceOnUse' x1='1100' y1='25' x2='1100' y2='777'%3E%3Cstop offset='0' stop-color='%23f000e8'/%3E%3Cstop offset='1' stop-color='%23160083'/%3E%3C/linearGradient%3E%3ClinearGradient id='l' gradientUnits='userSpaceOnUse' x1='1150' y1='25' x2='1150' y2='777'%3E%3Cstop offset='0' stop-color='%23E0F'/%3E%3Cstop offset='1' stop-color='%23007'/%3E%3C/linearGradient%3E%3C/defs%3E%3Cg %3E%3Crect fill='url(%23a)' width='1200' height='800'/%3E%3Crect fill='url(%23b)' x='100' width='1100' height='800'/%3E%3Crect fill='url(%23c)' x='200' width='1000' height='800'/%3E%3Crect fill='url(%23d)' x='300' width='900' height='800'/%3E%3Crect fill='url(%23e)' x='400' width='800' height='800'/%3E%3Crect fill='url(%23f)' x='500' width='700' height='800'/%3E%3Crect fill='url(%23g)' x='600' width='600' height='800'/%3E%3Crect fill='url(%23h)' x='700' width='500' height='800'/%3E%3Crect fill='url(%23i)' x='800' width='400' height='800'/%3E%3Crect fill='url(%23j)' x='900' width='300' height='800'/%3E%3Crect fill='url(%23k)' x='1000' width='200' height='800'/%3E%3Crect fill='url(%23l)' x='1100' width='100' height='800'/%3E%3C/g%3E%3C/svg%3E");
    background-attachment: fixed;
    background-size: cover;
    /* background by SVGBackgrounds.com */

    h1 {
        text-align: center;
        font-size: 47px;
        text-shadow: 0px 10px 10px black;
        cursor: pointer;
        user-select: none;
        transition: text-shadow 0.5s;
    }

    h1:hover {
        text-shadow: 0px 4px 15px black;
    }

    input.log-input {
        display: block;
        margin: auto;
        width: 60%;
        height: 40px;
        background-color: transparent;
        border: none;
        border-bottom: solid;
        border-bottom-color: white;
        outline: none;
        font-size: 22px;
        margin-bottom: 15px;
        transition: width 0.5s;
        color: black;
    }

    input:focus {
        border-bottom-color: black;
        width: 85%;
        color: white;
    }

    ::placeholder {
        color: black;
    }

    label#conditions {
        margin-bottom: 0% !important;

        input#conditions-box {
            display: inline-block;
        }
    }

    input#register-btn {
        width: 100%;
        height: 45px;
        font-weight: bold;
        background-color: black;
        color: white;
        border: none;
        border-radius: 7px;
        cursor: pointer;
    }

}
</style>
