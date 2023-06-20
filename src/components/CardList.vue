<template>
    <div class="row">
        <SingleCard v-for="card in cardList"
            :name="card.name"
            :type="card.archetype"
            :image="card.image_url"
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
            cardList : [],
            imageList : []
        }
    },
    components:{
        SingleCard
    },

    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
            this.cardList = response.data.data;
            this.imageList = response.data.data[1].card_images;
            console.log(this.imageList)
        })
    }
}
</script>

<style lang="">
    
</style>