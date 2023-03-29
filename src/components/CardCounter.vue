<script>
import { store } from '../store';
export default {
    name: 'CardCounter',
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <div class="row d-flex align-items-center mx-2">
        <div class="col">
            <h3 class="px-4">Found {{ store.charactersFound }} cards</h3>
        </div>
    </div>
</template>



<style lang="scss" scoped>
div .row {
    background-color: #212529;
    height: 80px;

    h3 {
        color: white;
    }
}
</style>