<script>
import axios from 'axios';
import { store } from '../store';
import CardApp from './CardApp.vue';
export default {
    nome: 'CardsList',
    components: {
        CardApp
    },
    data() {
        return {
            store,
            characters: []
        }
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php').then((response) => {
            console.log(response);
            this.store.characters = response.data.data;
            this.store.charactersFound = response.data.data.length;
            
        })
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