<script>

import CardApp from './CardApp.vue';
export default {
    nome: 'CardsList',
    components: {
        CardApp
    }
}
</script>

<template>
    <div class="row row-cols-5 mx-0">
        <div class="col mb-4 px-2" v-for="character in store.characters.slice(0, 15)">
            <CardApp 
            :img="character.card_images[0].image_url" 
            :name="character.name" 
            :type="character.archetype" />
        </div>
    </div>
</template>


<style lang="scss" scoped></style>