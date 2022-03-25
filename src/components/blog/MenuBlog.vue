<template>
    <!-- categorie -->
    <div>
        <ul>
            <li
                class="categories"
                v-for="(item,index) in menu"
                :key ="index"
            >
                <a href="">{{item.title}}</a>
            </li>
        </ul>
    </div>
    <!-- /categorie -->

</template>


<script>
    export default {
        name: 'menu-blog',
        props: {
            menu: Array,
        }
    }
</script>

<style scoped>

    li{
        display: inline-block;
        padding-right: 20px;
    }

    a{
        text-decoration: none;
    }

    .categories{
        font-size: 14px;
        margin-bottom: 20px;
        font-weight:700;
        color: white
    }


</style>