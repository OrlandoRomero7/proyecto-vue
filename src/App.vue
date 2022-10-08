<script setup>
import Title from './components/Title.vue';
import Login from './components/Login.vue'
import Formulario from './components/Formulario.vue';
</script>
<template >
    
    <Title titulo="Mi Red Social" ></Title>
    <div v-if=!estadoBoton>
        <Formulario v-on:clicked="onClickChild" ></Formulario>
    </div>
    <Login v-else v-bind:nombre="nombreUsuario"></Login>

    
</template>
<script>
export default { 
    components:{
        Title,
        Formulario,
        Login,
    },
    data(){
        return{
            nombreUsuario: '',
            estadoBoton: '',
        }
        
    },
    methods: {
        onClickChild (value1, value2) {
         this.nombreUsuario=value1;
         this.estadoBoton=value2;
        }   
    },
    
}


</script>
<style >
    *{
        margin: 0;
        padding: 0;
        

    }
    html{
        display: flex;
        justify-content: center;
        background-color: black;
    }
    
    
    
    
</style>
