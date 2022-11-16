    <script>
    export default {
    name:'AppJumbotron'
    }
    </script>

<template>
    <div class="wrapper">
        <div class="container"><p>we</p></div>
    </div>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    .wrapper{
        width: 100%;
        background-color: black;
    }
    .container{
        margin: 0 auto;
        width:$container-width;
        height: 100px;
        color: white;
    }
</style>