<template>
    <div id="login-body">
        <h1 class="sign-title" style="text-align: center;">Welcome Back!</h1>
        <div v-if="screenWidth <= 1070"
            style="width: 60%; display: flex; flex-direction: column; margin: auto;text-align: right;">
            <a style="text-decoration: none;color:#EE006A" id="login-link" href="#signup">First Datebook?</a>
        </div>
        <br>
        <form>
            <input class="log-input" required placeholder="Email" type="email" name="logemail">
            <input class="log-input" required placeholder="Password" type="password" name="logpassword">
            <div style="width: 60%; display: flex; flex-direction: column; margin: auto;text-align: justify;">
                <!-- <label style="color: #EE006A;cursor: pointer;" for="remember-box" id="remember">
                    <input required type="checkbox" name="remember" id="remember-box">
                    Remember Me
                </label> -->
                <br>
                <br>
                <input id="login-btn" type="button" value="SEND">
            </div>
        </form>
    </div>
</template>
  
<script>
export default {
    name: 'LogInComponent',
    data() {
        return {
            screenWidth: window.innerWidth
        }
    }
}
</script>
  
<style lang="scss" scoped>
div#login-body {
    display: block;
    flex-direction: column;
    align-items: center;
    width: 100%;
    background-color: #000000;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 2000 1500'%3E%3Cdefs%3E%3Crect stroke='%23000000' stroke-width='0.9' width='1' height='1' id='s'/%3E%3Cpattern id='a' width='3' height='3' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cuse fill='%23242424' href='%23s' y='2'/%3E%3Cuse fill='%23242424' href='%23s' x='1' y='2'/%3E%3Cuse fill='%23333333' href='%23s' x='2' y='2'/%3E%3Cuse fill='%23333333' href='%23s'/%3E%3Cuse fill='%233e3e3e' href='%23s' x='2'/%3E%3Cuse fill='%233e3e3e' href='%23s' x='1' y='1'/%3E%3C/pattern%3E%3Cpattern id='b' width='7' height='11' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cg fill='%23484848'%3E%3Cuse href='%23s'/%3E%3Cuse href='%23s' y='5' /%3E%3Cuse href='%23s' x='1' y='10'/%3E%3Cuse href='%23s' x='2' y='1'/%3E%3Cuse href='%23s' x='2' y='4'/%3E%3Cuse href='%23s' x='3' y='8'/%3E%3Cuse href='%23s' x='4' y='3'/%3E%3Cuse href='%23s' x='4' y='7'/%3E%3Cuse href='%23s' x='5' y='2'/%3E%3Cuse href='%23s' x='5' y='6'/%3E%3Cuse href='%23s' x='6' y='9'/%3E%3C/g%3E%3C/pattern%3E%3Cpattern id='h' width='5' height='13' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cg fill='%23484848'%3E%3Cuse href='%23s' y='5'/%3E%3Cuse href='%23s' y='8'/%3E%3Cuse href='%23s' x='1' y='1'/%3E%3Cuse href='%23s' x='1' y='9'/%3E%3Cuse href='%23s' x='1' y='12'/%3E%3Cuse href='%23s' x='2'/%3E%3Cuse href='%23s' x='2' y='4'/%3E%3Cuse href='%23s' x='3' y='2'/%3E%3Cuse href='%23s' x='3' y='6'/%3E%3Cuse href='%23s' x='3' y='11'/%3E%3Cuse href='%23s' x='4' y='3'/%3E%3Cuse href='%23s' x='4' y='7'/%3E%3Cuse href='%23s' x='4' y='10'/%3E%3C/g%3E%3C/pattern%3E%3Cpattern id='c' width='17' height='13' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cg fill='%23515151'%3E%3Cuse href='%23s' y='11'/%3E%3Cuse href='%23s' x='2' y='9'/%3E%3Cuse href='%23s' x='5' y='12'/%3E%3Cuse href='%23s' x='9' y='4'/%3E%3Cuse href='%23s' x='12' y='1'/%3E%3Cuse href='%23s' x='16' y='6'/%3E%3C/g%3E%3C/pattern%3E%3Cpattern id='d' width='19' height='17' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cg fill='%23000000'%3E%3Cuse href='%23s' y='9'/%3E%3Cuse href='%23s' x='16' y='5'/%3E%3Cuse href='%23s' x='14' y='2'/%3E%3Cuse href='%23s' x='11' y='11'/%3E%3Cuse href='%23s' x='6' y='14'/%3E%3C/g%3E%3Cg fill='%23585858'%3E%3Cuse href='%23s' x='3' y='13'/%3E%3Cuse href='%23s' x='9' y='7'/%3E%3Cuse href='%23s' x='13' y='10'/%3E%3Cuse href='%23s' x='15' y='4'/%3E%3Cuse href='%23s' x='18' y='1'/%3E%3C/g%3E%3C/pattern%3E%3Cpattern id='e' width='47' height='53' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cg fill='%23EE006A'%3E%3Cuse href='%23s' x='2' y='5'/%3E%3Cuse href='%23s' x='16' y='38'/%3E%3Cuse href='%23s' x='46' y='42'/%3E%3Cuse href='%23s' x='29' y='20'/%3E%3C/g%3E%3C/pattern%3E%3Cpattern id='f' width='59' height='71' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cg fill='%23EE006A'%3E%3Cuse href='%23s' x='33' y='13'/%3E%3Cuse href='%23s' x='27' y='54'/%3E%3Cuse href='%23s' x='55' y='55'/%3E%3C/g%3E%3C/pattern%3E%3Cpattern id='g' width='139' height='97' patternUnits='userSpaceOnUse' patternTransform='rotate(169 1000 750) scale(17.25) translate(-942.03 -706.52)'%3E%3Cg fill='%23EE006A'%3E%3Cuse href='%23s' x='11' y='8'/%3E%3Cuse href='%23s' x='51' y='13'/%3E%3Cuse href='%23s' x='17' y='73'/%3E%3Cuse href='%23s' x='99' y='57'/%3E%3C/g%3E%3C/pattern%3E%3C/defs%3E%3Crect fill='url(%23a)' width='100%25' height='100%25'/%3E%3Crect fill='url(%23b)' width='100%25' height='100%25'/%3E%3Crect fill='url(%23h)' width='100%25' height='100%25'/%3E%3Crect fill='url(%23c)' width='100%25' height='100%25'/%3E%3Crect fill='url(%23d)' width='100%25' height='100%25'/%3E%3Crect fill='url(%23e)' width='100%25' height='100%25'/%3E%3Crect fill='url(%23f)' width='100%25' height='100%25'/%3E%3Crect fill='url(%23g)' width='100%25' height='100%25'/%3E%3C/svg%3E");
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

    form {
        background-color: rgb(255, 255, 255);
        width: 60%;
        display: block;
        margin: auto;
        padding: 10px;
        border-radius: 15px;

        input.log-input {
            display: block;
            margin: auto;
            width: 60%;
            height: 40px;
            background-color: transparent;
            border: none;
            border-bottom: solid;
            border-bottom-color: black;
            outline: none;
            font-size: 22px;
            margin-bottom: 15px;
            transition: width 0.5s;
            color: black;
        }

        input:focus {
            border-bottom-color: blueviolet;
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

        input#login-btn {
            width: 100%;
            height: 45px;
            font-weight: bold;
            background-color: black;
            color: white;
            border: none;
            border-radius: 7px;
            cursor: pointer;
            background-color: #ff0000;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100%25' height='100%25' viewBox='0 0 1200 800'%3E%3Cdefs%3E%3ClinearGradient id='a' gradientUnits='userSpaceOnUse' x1='600' y1='25' x2='600' y2='777'%3E%3Cstop offset='0' stop-color='%23ff0000'/%3E%3Cstop offset='1' stop-color='%23E0F'/%3E%3C/linearGradient%3E%3ClinearGradient id='b' gradientUnits='userSpaceOnUse' x1='650' y1='25' x2='650' y2='777'%3E%3Cstop offset='0' stop-color='%23fd0017'/%3E%3Cstop offset='1' stop-color='%23d800f3'/%3E%3C/linearGradient%3E%3ClinearGradient id='c' gradientUnits='userSpaceOnUse' x1='700' y1='25' x2='700' y2='777'%3E%3Cstop offset='0' stop-color='%23fc002e'/%3E%3Cstop offset='1' stop-color='%23c300e6'/%3E%3C/linearGradient%3E%3ClinearGradient id='d' gradientUnits='userSpaceOnUse' x1='750' y1='25' x2='750' y2='777'%3E%3Cstop offset='0' stop-color='%23fa0046'/%3E%3Cstop offset='1' stop-color='%23ad00da'/%3E%3C/linearGradient%3E%3ClinearGradient id='e' gradientUnits='userSpaceOnUse' x1='800' y1='25' x2='800' y2='777'%3E%3Cstop offset='0' stop-color='%23f9005d'/%3E%3Cstop offset='1' stop-color='%239700ce'/%3E%3C/linearGradient%3E%3ClinearGradient id='f' gradientUnits='userSpaceOnUse' x1='850' y1='25' x2='850' y2='777'%3E%3Cstop offset='0' stop-color='%23f70074'/%3E%3Cstop offset='1' stop-color='%238200c1'/%3E%3C/linearGradient%3E%3ClinearGradient id='g' gradientUnits='userSpaceOnUse' x1='900' y1='25' x2='900' y2='777'%3E%3Cstop offset='0' stop-color='%23f6008b'/%3E%3Cstop offset='1' stop-color='%236c00b5'/%3E%3C/linearGradient%3E%3ClinearGradient id='h' gradientUnits='userSpaceOnUse' x1='950' y1='25' x2='950' y2='777'%3E%3Cstop offset='0' stop-color='%23f400a2'/%3E%3Cstop offset='1' stop-color='%235700a8'/%3E%3C/linearGradient%3E%3ClinearGradient id='i' gradientUnits='userSpaceOnUse' x1='1000' y1='25' x2='1000' y2='777'%3E%3Cstop offset='0' stop-color='%23f300b9'/%3E%3Cstop offset='1' stop-color='%2341009c'/%3E%3C/linearGradient%3E%3ClinearGradient id='j' gradientUnits='userSpaceOnUse' x1='1050' y1='25' x2='1050' y2='777'%3E%3Cstop offset='0' stop-color='%23f100d1'/%3E%3Cstop offset='1' stop-color='%232b0090'/%3E%3C/linearGradient%3E%3ClinearGradient id='k' gradientUnits='userSpaceOnUse' x1='1100' y1='25' x2='1100' y2='777'%3E%3Cstop offset='0' stop-color='%23f000e8'/%3E%3Cstop offset='1' stop-color='%23160083'/%3E%3C/linearGradient%3E%3ClinearGradient id='l' gradientUnits='userSpaceOnUse' x1='1150' y1='25' x2='1150' y2='777'%3E%3Cstop offset='0' stop-color='%23E0F'/%3E%3Cstop offset='1' stop-color='%23007'/%3E%3C/linearGradient%3E%3C/defs%3E%3Cg %3E%3Crect fill='url(%23a)' width='1200' height='800'/%3E%3Crect fill='url(%23b)' x='100' width='1100' height='800'/%3E%3Crect fill='url(%23c)' x='200' width='1000' height='800'/%3E%3Crect fill='url(%23d)' x='300' width='900' height='800'/%3E%3Crect fill='url(%23e)' x='400' width='800' height='800'/%3E%3Crect fill='url(%23f)' x='500' width='700' height='800'/%3E%3Crect fill='url(%23g)' x='600' width='600' height='800'/%3E%3Crect fill='url(%23h)' x='700' width='500' height='800'/%3E%3Crect fill='url(%23i)' x='800' width='400' height='800'/%3E%3Crect fill='url(%23j)' x='900' width='300' height='800'/%3E%3Crect fill='url(%23k)' x='1000' width='200' height='800'/%3E%3Crect fill='url(%23l)' x='1100' width='100' height='800'/%3E%3C/g%3E%3C/svg%3E");
            background-attachment: fixed;
            background-size: cover;
        }
    }
}
</style>
  