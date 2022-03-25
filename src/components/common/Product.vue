<template>
    <div class="container">
        <div class="image"></div>
        <div>
            <h4 class="name">{{this.name}}</h4>
            <p class="price">{{this.price}}</p>
            <p class="category">{{ this.category}}</p>
        </div>
    </div>
</template>

<script>

    export default{
        name: 'prod-uct',
        props:{
            name: String,
            price : String,
            category : String,
            img: String,
            url: String
        }
    }
</script>

<style scoped>
    .container{
        text-align: center;    
    }
    .image{
        width:200px;
        height: 200px;
        background-color: aliceblue;
    }

    .name{
        
    }

    .price{
        
    }

    
</style>