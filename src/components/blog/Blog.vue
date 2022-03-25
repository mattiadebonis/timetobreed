<template>

    <header>

        <Header />  

        <div class="menu">
            <MenuBlog  
                :menu = "this.categories"
            />
        </div>    
    </header>
    
    <main>
        <section id="article">
            <LatestArticle />
        </section>
        
        <section>
            <SectionBlog />
        </section>

    </main>

    <footer>
        <Footer />
    </footer>
  
</template>

<script>
    import Header from '../common/Header.vue'
    
    import MenuBlog from './MenuBlog.vue';

    import SectionBlog from './SectionBlog.vue';
    import LatestArticle from '../home/LatestArticle.vue';

    import Footer from '../common/Footer.vue'

    export default {
        name: 'App',
        components: {
            //header
            Header,
            MenuBlog,
            //main
            LatestArticle,
            SectionBlog,

            //footer
            Footer
        },
        data: function(){
            return{
                categories:[
                    {
                        title:"News",
                        url: "#"
                    },
                    {
                        title:"Tutorial",
                        url: "#"
                    },
                    {
                        title:"Prodotti",
                        url: "#"
                    }
                ],
                
                tags:[
                    {
                        title:"Falene",
                        url: "#"
                    },
                    {
                        title:"Shop",
                        url: "#"
                    },
                    {
                        title:"Time to breed",
                        url: "#"
                    }
                ]
            }
        }
    }
</script>

<style>

    header{
        background-color: yellowgreen;
    }

    #article{
        padding: 150px 20%; 
        background-color: yellowgreen;
    }

    .menu{
        text-align: center;
        padding:% 20% 0 20%;
    }
    
</style>