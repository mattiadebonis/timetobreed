<template>
    <div>
        <h2>Feedback</h2>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolorem maiores totam repudiandae dolor error unde non laudantium nobis perspiciatis inventore ducimus nemo, amet, mollitia corporis facere deserunt. At debitis id, velit voluptates voluptas sunt ipsam laboriosam maiores atque, beatae quasi repellendus voluptatum molestiae facere. Eum odit in ipsam perferendis odio? Vero, accusamus architecto beatae maxime aspernatur blanditiis explicabo ut animi?</p>
        <ul>
            <li
                class="reviews"
                v-for="(item,index) in reviews"
                :key="index"
            >
                <Review
                    :name = "item.name"
                    :text = "item.text"
                    :img = "item.img"
                    :url = "item.url"
                />
            </li>
        </ul>
        
        <div class="number-container">
            <div class="section-about">
                <p>100% positive feedback on ebay</p>
            </div>
            <div class="section-about">
                <p>50+ countries reached worldwide</p>
            </div>
            <div class="section-about">
                <p>99%+ parcels arrived safely</p>
            </div>
        </div>
    </div>
</template>

<script>

    import Review from '../common/Review.vue'

    export default{

        // name
        name: 'feed-back',

        // components
        components:{
            Review
        },
        
        // data
        data: function(){
            return {
                reviews : [
                    {
                        name : "Tizo",
                        text : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, explicabo! Numquam expedita libero ipsa amet aspernatur qui hic provident consequatur.",
                        url : "#",
                        img : "#"
                    },
                    {
                        name : "Caio",
                        text : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, explicabo! Numquam expedita libero ipsa amet aspernatur qui hic provident consequatur.",
                        url : "#",
                        img : "#"
                    },
                    {
                        name : "Sempronio",
                        text : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, explicabo! Numquam expedita libero ipsa amet aspernatur qui hic provident consequatur.",
                        url : "#",
                        img : "#"
                    },
                    
                    
                ]
            }
        },

    }

</script>

<style scoped>

    ul{
        display: flex;    
        flex-wrap: wrap;
    }

    .reviews{
        display: inline-block;
        list-style: none;
        margin: 10px;
        width: 25%;
    }
    
</style>
