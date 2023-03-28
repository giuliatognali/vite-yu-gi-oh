<script>
export default {
    nome: 'CardApp',
    props:{
        img: String,
        name: String,
        type: String
    }

}
</script>


<template>
    <div class="ms-card text-center d-flex flex-column align-items-center"  >
        <div class="img">
            <img :src="img" alt="">
        </div>
        <h5 class="my-3">{{ name }}</h5>
        <p>{{ type }}</p>
    </div>


</template>



<style lang="scss" scoped>
@use '../assets/scss/_partial/variables' as *;
.ms-card {
    background-color: $bg-color;
    justify-content: space-between;
    height: 100%;

    img{
        display: inline-block;
    }
    h5{
        color: white;
    }
}
</style>