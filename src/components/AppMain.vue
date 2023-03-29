<script>
import CardsList from './CardsList.vue';
import CardSelect from './CardSelect.vue';
import CardCounter from './CardCounter.vue';
export default {
    name: 'AppMain',
    components: {
        CardSelect,
        CardsList,
        CardCounter
    }

}
</script>

<template>
    <div class="ms-container pt-1">
        <CardSelect />
        <div class="small-container p-5">
        <CardCounter />
        <CardsList />
    </div>
    </div>
</template>



<style lang="scss" scoped>
@use '../assets/scss/_partial/variables' as *;
.ms-container {
    background-color: $bg-color;
    padding: 0 100px;
    .small-container{
        background-color: white;

    }

}
</style>