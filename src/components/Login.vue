<script setup>
    import Post from './Post.vue'
</script>
<template lang="">
    <div class="post">
        <div class="publicar">
                <h3>Nueva Publicación</h3>
                <textarea type="text" v-model="descripcionPost" placeholder="Qué estas pensando?"></textarea>
                <button v-on:click="accionPublicar">Publicar</button>
        </div>
        <ul>
        <li v-for="descripcionPost in descripcionPosts" v-bind:key="descripcionPost.key">
            <Post v-bind:user="nombre" v-bind:user-Post="descripcionPost" ></Post>
        </li>
    </ul>
        
    </div>
        

</template>
<script>

export default {
    methods:{
        
        accionPublicar(){
            this.descripcionPosts.push(this.descripcionPost);
        },
        
        
    },
    data(){
        return{
            
            
            descripcionPost: '',
            descripcionPosts: [],


        }
    },
    components:{
        Post
    },
    props:['nombre']
    
}
</script>
<style scoped>
    
    body{
    margin: 0;
    padding: 0;
    background: url(../assets/images/fondoLogin.jpg);
    }
    
    .avatar {
        width: 100px;
        height: 100px;
        border-radius: 50%;
        position: absolute;
        top: -10%;
        left: calc(50% - 50px);
        background-color: white;
    }
    h1 {
        margin: 0;
        padding: 0;
        text-align: center;
        font-size: 22px;
    }

    
    .publicar{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        width: 350px;
        height: 200px;
        border-style: solid;
        background-color: gray;
    
        
    }
    .publicar textarea{
        
        width: 330px;
        height: 100px;
        
    }
    .publicar button{
        margin-top: 10px;
        width: 300px;
        border-radius: 10px;
        background-color: cadetblue;
    }
    
    
</style>
