<template>
    <div class="review-container">
        <h3>{{this.name}}</h3>
        <p>{{this.text}}</p>
    </div>
</template>

<script>

    export default{
        name: 're-view',
        props:{
            name: String,
            text : String,
            img: String,
            url: String
        }
    }
</script>

<style scoped>

    .review-container{
        background-color: lightgray;
        padding: 30px;
        display: inline-block;
    }

    h3{
        font-size: 16px;
    }

    p{
        font-size: 14px;
    }
    
</style>