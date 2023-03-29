<script>

    export default {
        name: 'AppHeader'
        
    }
</script>

<template>
    <div class="ms-container d-flex align-items-center">
        <div class="logo">
            <img src="img/logo.png" alt="">
        </div>
            <h1 class="mb-0">Yu-Gi-Oh Api</h1>   
    </div>
</template>



<style lang="scss" scoped>
.ms-container{
    height: 105px;
    padding: 10px;
    .logo{
        height: 30px;
        padding: 0 30px;
        img{
            height: 100%;
        }
    }
}

</style>