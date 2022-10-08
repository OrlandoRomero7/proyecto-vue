
<template >
    <div class="main__logout">
        
        <div class="post__benito">

            <div class="header__post">
                <img src="../assets/images/profile-user.png" width="30" height="30" />  
                <div class="items"> <h3>{{user}}</h3> </div>
            </div>

            <br>

            <hr>

            <img class="michi" src="../assets/images/michis.jpg" width="28%" height="250" />

            <br>

            <div class="reacciones">
                            
                <div class="items__reacciones"><img src="../assets/images/me-gusta.png" width="20" height="20"/></div>
                <div class="items__reacciones"><img src="../assets/images/burbuja-de-chat.png" width="20" height="20"/></div>
                <div class="items__reacciones"><img src="../assets/images/enviar.png" width="20" height="20"/></div>
                                
            </div>

            
            <div class="items__descripcion">
                <div><strong>{{user}}</strong></div>
                <div class="texto__descripcion"><p>{{userPost}}</p></div>
            </div>
        
            
                    
        </div>
                                 
    </div>

</template>
<script>
export default {
    
    
    props:[
        'user', 'userPost'
    ]
    
    
}
</script>

<style >
    *{
        margin: 0;
        padding: 0;
        box-sizing: inherit;
    }
    
    .main__logout{
        padding-top: 10%;
        height: 100vh;
        width: 100%;
    }
    .post__benito{
            
        background-color: antiquewhite;
        margin: 0 auto;
        border-radius: 10px;
        height: 500px;
        width: 350px;
        border-style: solid;
    }
    .header__post{
        display: flex;
        flex-direction: row;
        align-items: flex-start;
    
        margin: 2% 2%;
        height: 20px;
        width: 100%;
    }
    
    .items__descripcion{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin-left: 5px;
        
        
    }
    
    .items{
        margin-left: 2%;
    }
    .reacciones{
        display: flex;
        flex-direction: row;
            
    }
    .items__reacciones{
        margin-left: 3%;
    }
    p{
        font-size: 13px;
    }
    .michi{
        margin-top:2%;
        margin-left: 2%;
        margin-right: 2%;
        width: 95%;
    }
    
    
    
</style>