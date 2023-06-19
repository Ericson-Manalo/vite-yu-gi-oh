<template>
    <main>
        <h2>
            Main
        </h2>
        <h3>
            <CardList/>
        </h3>
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
<style lang="scss">
    
</style>