<script>
import axios from 'axios';
import CardApp from './CardApp.vue';
export default {
    nome: 'CardsList',
    components: {
        CardApp
    },
    data() {
        return {
            characters: []
        }
    },
    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php').then((response) => {
            console.log(response);
            this.characters = response.data.data;
        })
    }
}
</script>

<template>
    <div class="row row-cols-5 mx-0">
        <div class="col mb-4 px-3" v-for="character in characters.slice(0,15)">
            <CardApp  
            :img="character.card_images[0].image_url" 
            :name="character.name"
            :type="character.archetype"
            />
        </div>
    </div>
</template>


<style lang="scss" scoped>
</style>