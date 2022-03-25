<template>

    <div class="jumbotrone">

        <div class="jumbo-left">
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. </h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae eaque, nemo porro corrupti error accusamus laborum aspernatur molestias totam aut amet natus nisi possimus maiores, animi perspiciatis explicabo expedita dolorem ut libero deleniti non magni! Earum cum amet sunt, ratione voluptates asperiores ad ipsam, eum aspernatur, facilis culpa eius nesciunt.</p>
            <a href="#">Browse to Shop</a>
        </div>
        
        <div class="jumbo-right">
            <img src="" alt="">
        </div>

    </div>

</template>

<script>

export default{
    name: 'jumbo-tron',
}
</script>

<style scoped>

    .jumbotrone{
        display: flex;
        width: 100%;
        align-items: flex-start;
        justify-content:center;
    }
    
    .jumbo-left, .jumbo-right{
        width: 40%;
    }

    h1{
        font-size: 48px;
    }
    
</style>
