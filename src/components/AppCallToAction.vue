    <script>
    import blueLinks from '../data/blueLinks.js';
    export default {
        name:'AppCallToAction',
        data(){
            return{
                blueLinks
            }
        },
        methods:{
            getPathImage(imageName){
                return new URL(`../assets/img/${imageName}`, import.meta.url).href
            }
        }
    }
    </script>

<template>
  <div class="wrapper">
    <div class="container">
        <div class="col" v-for="(link,index) in blueLinks" :key="index">
            <div class="link">
                <div class="img-wrapper">
                    <img :src="getPathImage(link.url)" :alt="link.url">
                </div>
                <p>{{link.text}}</p>
            </div>
        </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
    @use '../styles/partials/_variables.scss' as *;
    @use '../styles/general.scss' as *;

    .wrapper{
        height: 300px;
        background-color: $primary-color ;
    }
    .container{
        width: 80%;
        display: flex;
        margin: 0 auto;
        height: 100%;
        .col{
            height: 100%;
            width: calc(100% / 5);
            display: flex;
            align-items: center;
        }
        .link{
            display: flex;
            padding: 30px;
            align-items: center;
            text-transform: uppercase;
            font-weight: 700;
            color: white;
            .img-wrapper{
                max-width: 100px;
                overflow: hidden;
                margin-right:10px ;
            }
            img{
                width: 100%;
            }
        }
        
    }
    

</style>