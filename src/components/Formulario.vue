<script setup>
    import Login from './Login.vue'
</script>
<template lang="">
    <div class="contenedor__login">
        <div class="login__box">
        <img src="../assets/images/cat.png">
        <h1>Login</h1>
        <form>
            <input type="text" placeholder="Usuario" v-model="nombreUsuario" >
            <input type="submit" value="Login" v-on:click="onClickButton">
        </form>
    </div>

    </div>
    
    
</template>
<script>
export default {
    
    data(){
        return{
            nombreUsuario: '',
            estadoBoton: true,
        }
    },
    methods:{
        onClickButton (event) {
        this.$emit('clicked',this.nombreUsuario, this.estadoBoton)
        }
        
    },
    components:{
        Login
    }
    
}
</script>

<style scoped>

.login__box{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10px;
    background-color: #333;
}
.login__box img{
    width: 100px;
    height: 100px;
    border-radius: 100px;
}
form{
    display: flex;
    flex-direction: column;
}
input{
 margin: .5rem 0;
 border-radius: 12px;
 padding: 5px 10px;   
}

</style>




<!-- <style scoped>
    .login__box{
        /* width: 320px;
        height: 420px; */
        background: #000;
        color: #fff;
        top: 50%;
        left: 50%;
        position: absolute;
        transform: translate(-50%, -50%);
        box-sizing: border-box;
        padding: 70px 30px;
        box-shadow: 20px 20px 20px rgb(156, 155, 155);
        

    }
    .login__box p {
        margin: 0;
        padding-top: 10%;
        font-weight: bold;
        font-size: 20px;
        text-align: start;
    }

    .login__box input {
        width: 100%;
    }

    .login__box input[type = "text"] {
        border: none;
        border-bottom: 1px solid #fff;
        background: transparent;
        outline: none;
        height: 40px;
        color: #fff;
        font-size: 16px;
        margin-top: 10%;
        font-family:'Gill Sans';
    }

    .login__box input[type = "submit"] {

        border: none;
        outline: none;
        height: 40px;
        background: #08b0ce;
        color: #fff;
        font-size: 18px;
        border-radius: 20px;
        margin-top: 50%;
    }

    .login__box input[type = "submit"]:hover {
        cursor: pointer;
        background: #fff;
        color: #000;
    }

    .login__box a {
        text-decoration: none;
        font-size: 12px;
        line-height: 20px;
        color: darkgrey;
    }

    .loginbox a:hover {
        color: #fff;
    }
    
</style> -->