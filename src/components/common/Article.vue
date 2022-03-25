<template>
        <div :class="isMain(type)">
            <p class="tag">{{ this.category}}</p>
            <p class="date">{{this.date}}</p>
            <h3>{{this.title}}</h3>
            <p>{{this.abstract}}</p>
        </div>

        <div :class="isImageMain(type)"></div>
</template>

<script>

    export default{
        name: 'arti-cle',
        props:{
            title: String,
            date : String,
            abstract : String,
            category : String,
            img: String,
            url: String,
            type: String,
            firstBig: Boolean
            
        },
        methods : {
            isMain : function(index){
                if(index == "0" && this.firstBig == true){
                    return "article-container-main"
                }else{
                    return "article-container-regular"
                }
            },

            isImageMain : function(index){
                if(index == "0" && this.firstBig == true){
                    return "image-container-main"
                }else{
                    return "image-container-regular"
                }
            }
        },
    }

</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Arvo&display=swap');
    
    .article-container-main{
        display: inline-block;
        width:50%;
    }

    .image-container-main{
        display: inline-block;
        background-color: aquamarine;
        border-radius: 15px;
        width: 45%;
        height: 250px;
        margin-left:10px;
    }

    .article-container-main > h3{
        font-size: 36px;
    }

    
    .article-container-regular > h3{
        font-size: 24px;

    }

    .tag{
        display: inline;
        font-size: 10px;
        background-color: red;
        padding: 3px 5px;
        color: white;
        border-radius: 10px;
    }

    .image-container-regular{
        display: inline-block;
        background-color: aquamarine;
        border-radius: 15px;
        width: 100%;
        height: 250px;
    }

    .date{
        font-family: 'Arvo', serif;
        display:inline;
        font-size: 10px;
        color: light-gray;
    }

</style>