<template>
    <footer>
        <!-- footer top -->
        <div class="footer-top">
            
            <!-- logo -->
            <div class="footer-section-menu">
                <img src="" alt="">
            </div>
            <!-- /logo -->

            <!--menu -->
            <div 
                class="footer-section-menu"
                v-for="index in 3" 
                :key="index"
            >
                <ul>
                    <li
                        v-for="(item,index) in footerMenu"
                        :key="index"
                    >
                        <a :href="item.url">{{item.title}}</a>
                    </li>
                </ul>   
            </div>
            <!--menu -->

            <!-- newsletter -->
            <div>
                <form action="">
                    <input type="email">
                    <input type="password">
                </form>
            </div>
            <!-- newsletter -->


        </div>
        <!-- /footer top -->

        <!-- footer bottom -->
        <div class="footer-bottom">
            <p>(c) All rights reserved</p>
            <p>Time to breed - P Iva 1234567789</p>
            <div>
                <img src="" alt="">
                <img src="" alt="">
                <img src="" alt="">
            </div>
        </div>
        <!-- footer bottom -->
        
    </footer>
    
</template>

<script>

export default{

    name: 'footer-page',

    data() {
        return{
            footerMenu: []
        }
    },

    created(){
        this.getFooterMenu()
    },

    methods:{
        getFooterMenu(){
            this.footerMenu = [
                {
                    title:"Pippo",
                    url: "#"
                },
                {
                    title:"Pluto",
                    url: "#"
                },
                {
                    title:"Paperino",
                    url: "#"
                }
            ]
            return 'Ciao'
        }
    }

}
</script>

<style scoped>
    footer{
        background-color: gray;
        color: white;
        padding: 5% 10% 0 10%;
    }

    a{
        text-decoration: none;
        color:white;
        margin-bottom: 10px;
    }

    a:hover{
        text-decoration: underline;
    }

    .footer-top{
        display: flex;
    }

    .footer-bottom{
        display: flex;
        justify-content: space-between;
        padding: 70px 0 20px 0;
    }

    .footer-section-menu{
        width: 15%;
    }

    .footer-section-newsletter{
        width:40%;
    }

    li{
        list-style: none;
    }

</style>
