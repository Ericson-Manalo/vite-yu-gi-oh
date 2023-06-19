<template>
    <main>
        <div class="main-container">
            <div class="row">
                <div class="col-12 m-auto">
                Found cards
            </div>
            </div>

            <CardList/>
        </div>

    </main>

</template>

<script>
import CardList from './CardList.vue';

export default {
    name: 'AppMain',
    data(){
        return{
        }
    },
    components:{
        CardList
    }
}
</script>
<style lang="scss" scoped>
    main{
        background-color: #d48f38;
        display: flex;
    }

    .main-container{
        background-color: #fff;
        width: 1000px;
        margin: 3rem auto;
        padding: 1.5rem;
    }

    div.col-12{
        background-color: #212529;
        color: white;
        padding: 1rem;
    }
</style>