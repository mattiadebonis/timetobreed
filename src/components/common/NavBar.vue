<template>
    <nav>
        <div>
            <!-- logo -->

            <img alt="Vue logo" src="assets/images/logo.png">
        </div>

        <!-- menu -->
        <div>
            <ul>
                <li
                    v-for="(item,index) in navBar"
                    :key="index"
                >
                    <a :href="item.url">{{item.title}}</a>
                </li>
            </ul>
        </div>

        <!-- button -->
        <ul>
            <li><a class="btn" href="#"></a>Cerca</li>
            <li><a class="btn" href="#"></a>Shop</li>
        </ul>
    </nav>
</template>

<script>

export default{
    name: 'nav-bar',
    data() {
        return{
            navBar: []
        }
    },
    created(){
        this.getNavBarItem()
    },
    methods:{
        getNavBarItem(){
            this.navBar = [
                {
                    title:"Shop",
                    url: "#"
                },
                {
                    title:"Blog",
                    url: "#"
                },
                {
                    title:"Tutorial",
                    url: "#"
                },
                {
                    title:"About",
                    url: "#"
                }
            ]
        }
    }
}
</script>

<style scoped>
    

    nav{
        display:flex;
        justify-content: space-around;
        align-items: center;
        height: 100px;

    }

    li{
        display: inline;
    }

    a{
        text-decoration: none;
        font-weight: 700;
        padding: 0 15px;
    }
    
    .btn{
        padding: 7 15px;    
        color: white;
    }

    .btn:hover{
        opacity: 0.2;
    }

    .btn-blue{
        background-color: blue;
    }

    .btn-green{
        background-color: green;
    }

    
</style>
