    <script>
    export default {
    name:'AppJumbotron'
    }
    </script>

<template>
    <div class="wrapper">
    </div>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    .wrapper{
        width: 100%;
        background-image: url('../assets/img/jumbotron.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        height: 600px;
    }
    .container{
        margin: 0 auto;
        width:$container-width;
        height: 100px;
        color: white;
    }
</style>