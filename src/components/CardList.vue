<template>
    <div class="row">
        <SingleCard v-for="card in cardList"
            :name="card.name"
            :type="card.archetype"
            :image="card.card_images.image_url_small"
        />  

    </div>

</template>

<script>
import SingleCard from './SingleCard.vue';
import axios from 'axios';


export default {
    name : 'CardList',
    data(){
        return{
            cardList : []
        }
    },
    components:{
        SingleCard
    },

    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
            this.cardList = response.data.data;
            console.log(response.data.data.card_images)
        })
    }
}
</script>

<style lang="">
    
</style>