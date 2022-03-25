<template>
    <div>
        <h2>Latest shop</h2>
        <div>
            <ul>
                <li 
                    class="product" 
                    v-for="(item,index) in products"
                    :key ="index"
                >
                    <Product
                        :category = "item.category"
                        :name = "item.name"
                        :price = "item.price"
                        :img = "item.img"
                        :url = "item.url"
                    />

                </li>
            </ul>
        </div>
    </div>
</template>

<script>

    import Product from '../common/Product.vue'

    export default{

        // name
        name: 'latest-shop',

        // components
        components:{
            Product
        },

        // data
        data: function(){
            return {
                products : [
                    {
                        name : "Prodotto 1",
                        price : "25,00€",
                        category : "categoria 1",
                        url : "#",
                        img : "#"
                    },
                    {
                        name : "Prodotto 2",
                        price : "2,00€",
                        category : "categoria 2",
                        url : "#",
                        img : "#"
                    },
                    {
                        name : "Prodotto 3",
                        price : "40,00€",
                        category : "categoria 3",
                        url : "#",
                        img : "#"
                    },
                    {
                        name : "Prodotto 4",
                        price : "30,00€",
                        category : "categoria 4",
                        url : "#",
                        img : "#"
                    },                    
                ]
            }
        }
    }

</script>

<style scoped>

    ul{
        display: flex;    
    }

    .product{
        display: inline-block;
        list-style: none;
        margin: 10px;
        width: 20%;
    }
    
</style>

