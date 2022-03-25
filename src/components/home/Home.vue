<template>

    <header>
        <Header />      
    </header>
  
    <main>
        <section id="jumbo">
            <Jumbo />
        </section>

        <section id="article">
            <LatestArticle />
        </section>
            
        <section id="shop">
            <LatestShop />
        </section>
            
        <section id="tutorial">
            <Tutorial />
        </section>

        <section id="feedback">
            <Feedback />    
        </section>
        
    </main>

    <footer>
        <Footer />
    </footer>
  
</template>

<script>
    import Header from '../common/Header.vue'

    import Jumbo from './/Jumbo.vue';
    import LatestArticle from './/LatestArticle.vue';
    import LatestShop from './/LatestShop.vue';
    import Tutorial from './/Tutorial.vue';
    import Feedback from './/Feedback.vue';

    import Footer from '../common/Footer.vue'


    export default {
        name: 'App',
        components: {
            //header
            Header,

            //main
            Jumbo,
            LatestArticle,
            LatestShop,
            Tutorial,
            Feedback,

            //footer
            Footer
        }
    }
</script>

<style>
    
    #jumbo, #article, #feedback, #about, #tutorial{
        margin: 150px 20%; 
    }

    #shop{
        padding: 50px 20%; 
        background-color:greenyellow;
    }

</style>