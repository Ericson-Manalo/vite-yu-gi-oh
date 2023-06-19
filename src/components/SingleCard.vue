<template>
    <div class="col-3 card-container">
        <img :src="image" alt="">
        <h4>
            {{ name }}
        </h4>
        <p>
            {{ type }}
        </p>
    </div>
</template>

<script>
export default {
    name : 'SingleCard',
    data(){
        return{

        }
    },
    props:{
        name: String,
        type: String,
        image: String
    }
    
}
</script>

<style lang="scss" scoped>
    div.card-container{
        background-color: #d48f38;
        gap: .5rem;
        text-align: center;
    }

    h4{
        text-transform: uppercase;
        color: white;
        font-size: 1rem;
    }
</style>