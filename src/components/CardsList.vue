<script>
import CardApp from './CardApp.vue';
export default {
    nome: 'CardsList',
    components:{
        CardApp
    }

}
</script>

<template>
<div class="row row-cols-5 mx-0">
    <div class="col px-0">
        <CardApp />

    </div>
    </div>
</template>


<style lang="scss" scoped>
div {
    background-color: white;
}
</style>