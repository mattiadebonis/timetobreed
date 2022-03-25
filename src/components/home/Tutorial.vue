<template>
    <div>
        <h2>Nemo totam nesciunt similique! Itaque, labore tenetu.</h2>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nemo totam nesciunt similique! Itaque, labore tenetur expedita fugiat possimus quasi voluptatem iure, quisquam, odio suscipit autem doloremque sint reiciendis est beatae ipsum. Ab ipsum labore illo hic, adipisci cum, molestias recusandae corporis vitae fugiat quam minima deleniti veniam ipsam fuga dicta.</p>
        <ul>
            <li
                class="tutorial"
                v-for="(item,index) in tutorials"
                :key="index"
            >
                <Article
                    :category = "item.category"
                    :title = "item.title"
                    :abstrack = "item.abstract"
                    :img = "item.img"
                    :url = "item.url"
                />
            </li>
        </ul>
    </div>
</template>

<script>

    import Article from '../common/Article.vue'

    export default{

        // name
        name: 'tuto-rial',

        // components
        components:{
            Article
        },

        // data
        data: function(){
            return {
                tutorials : [
                    {
                        title : "Tutorial 1",
                        abstract : "Lorem20S",
                        category : "categoria 1",
                        url : "#",
                        img : "#"
                    },
                    {
                        title : "Tutorial 2",
                        abstract : "Lorem ipsum 2",
                        category : "categoria 2",
                        url : "#",
                        img : "#"
                    },
                    {
                        title : "Tutorial 3",
                        abstract : "Lorem ipsum 3",
                        category : "categoria 3",
                        url : "#",
                        img : "#"
                    }    
                ]
            }
        },

    }

</script>

<style scoped>
    h2{
        font-size: 42px;
    }
    ul{
        display: flex;    
        flex-wrap: wrap;
    }

    .tutorial{
        display: inline-block;
        list-style: none;
        margin: 10px;
        width: 25%;
    }
    
</style>
