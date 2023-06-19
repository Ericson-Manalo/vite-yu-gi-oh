<template>
    <div class="row">
        <SingleCard v-for="card in cardList"
            :name="card.name"
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
        }
    },
    components:{
        SingleCard
    },

    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
            console.log(response.data.data);
            this.cardList = response.data.data;
        })
    }
}
</script>

<style lang="">
    
</style>