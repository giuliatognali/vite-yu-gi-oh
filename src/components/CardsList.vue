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
    <div>
        CONTENITORE CARTE
        <CardApp />
    </div>
</template>


<style lang="scss" scoped>
div {
    background-color: white;
}
</style>