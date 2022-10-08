<template >
    <h1 class="titulo">{{titulo}}</h1>
</template>
<script>
export default {
    props:{
        titulo: {
            type: String,
            required: true
        },
        

    },
    data(){
        return{
            text: ' ',
        }
    }
    
}
</script>
<style >
    .titulo{
        color: white;
        font-size: 40px;
    }
    
</style>