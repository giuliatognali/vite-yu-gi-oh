<script>
    export default {
        name: 'CardSelect'
        
    }
</script>

<template>
        <label for="archetype" class="d-none" >Choose type:</label>
        <select class="form-select my-4 ms-3" id="archetype" name="archetype">
            <option value="Alien">Alien</option>
            <option value="saab">Non-alien</option>
        </select>
</template>



<style lang="scss" scoped>
    select{
        width: 240px;
    }
</style>