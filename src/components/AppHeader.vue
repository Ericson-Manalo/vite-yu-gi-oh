<template>
    <header>
        <div>
            <img src="../assets/images/ygoprodeck_header_logo.png" alt="Ygo Logo">
        </div>
        <div>
            <h1 class="ms-4 fs-1">
                Yu-Gi-Oh Api
            </h1>
        </div>
    </header>
</template>

<script>
export default {
    name: 'AppHeader',
    data(){
        return{

        }
    }
}
</script>

<style lang="scss">
    header{
        display: flex;
        align-items: center;
        padding: 1rem;
        background-color: #fff;
    }
</style>