<script>
import CardsList from './CardsList.vue';
import CardSelect from './CardSelect.vue';
import CardCounter from './CardCounter.vue';
export default {
    name: 'AppMain',
    components: {
        CardsList,
        CardSelect,
        CardCounter
    }

}
</script>

<template>
    <div class="ms-container pt-1">
        <CardSelect />
        <CardCounter />
        <CardsList />
    </div>
</template>



<style lang="scss" scoped>
.ms-container {
    height: 100vh;
    background-color: #d48f38;
    padding: 0 160px;

}
</style>