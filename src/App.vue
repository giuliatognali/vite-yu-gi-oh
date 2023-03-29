<script>
import axios from 'axios';

import { store } from './store';

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain
  },
  created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php').then((response) => {
            console.log(response);
            this.store.characters = response.data.data;
            this.store.charactersFound = response.data.data.lenght;
        })

    }
}
</script>

<template>
<AppHeader />
<AppMain />
</template>

<style lang="scss" scoped></style>
