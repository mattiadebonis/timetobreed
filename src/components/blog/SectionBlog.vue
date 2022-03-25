<template>
    <div>
        <div>
            <ul>
                <li 
                    class="article" 
                    v-for="(item,index) in articles"
                    :key ="index"
                >
            
                    <Article
                        :category = "item.category"
                        :date = "item.date"
                        :title = "item.title"
                        :abstract = "item.abstract"
                        :img = "item.img"
                        :url = "item.url"
                        :type="index"
                        :firstBig="false"
                    />
                </li>
            </ul>
        </div>
    </div>
</template>


<script>
    import Article from '../common/Article.vue'
    export default {
        name: 'section-blog',
        components: {
            Article,
        },
        // data
        data: function(){
            return {
                articles : [
                    {
                        title : "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                        abstract : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, corporis nulla velit sunt deleniti odit ab ad accusamus adipisci officia?",
                        category : "categoria 1",
                        date: "3 march 2021",
                        url : "#",
                        img : "#"
                    },
                    {
                        title : "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                        abstract : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, corporis nulla velit sunt deleniti odit ab ad accusamus adipisci officia?",
                        category : "categoria 2",
                        date: "30 april 2022",
                        url : "#",
                        img : "#"
                    },
                    {
                        title : "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
                        abstract : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, corporis nulla velit sunt deleniti odit ab ad accusamus adipisci officia?",
                        category : "categoria 3",
                        date : "6 december 2021",
                        url : "#",
                        img : "#"
                    },
                ]
            }
        },
    }
</script>

<style scoped>

</style>