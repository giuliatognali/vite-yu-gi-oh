<script>
import axios from 'axios';

    export default {
        name: 'CardSelect',
        data(){
            return{
                archetypes: []
            }
        },
        created(){
            console.log('created');
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((response) => {
                console.log(response.data);
                this.archetypes = response.data;
            });
        }
    }
</script>

<template>
        <label for="archetype" class="d-none" >Choose type:</label>
        <select class="form-select my-4 ms-3" id="archetype" name="archetype">
            <option value="">Select Archetype</option>
            <option v-for="arch in archetypes" >{{arch.archetype_name}}</option>
        </select>
</template>



<style lang="scss" scoped>
    select{
        width: 240px;
    }
</style>