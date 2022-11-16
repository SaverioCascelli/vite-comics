<script>
import footerList from '../data/footerLists';
import VerticalList from './VerticalList.vue';

export default {

    name: 'TopFooter',
    components:{
        VerticalList
    },
    data(){
        return{
            footerList,
        }
    }
}
</script>

<template>
    <div class="wrapper">
        <div class="dc-layer">
            <div class="container">
                <VerticalList
                class="lists"
                v-for="(list,index) in footerList"
                :key="index"
                :listObj="list"
                />
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
    @use "../styles/general.scss" as *;

    .wrapper{
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        height: 500px;
        overflow: hidden;
        .dc-layer{
            background-image: url("dc-logo-bg.png");
            margin: 0 auto;
            height: 100%;
            width: 80%;
            background-size: 40%;
            background-position-x: right;
            background-position-y: 50% ;
            background-repeat: no-repeat;
            .lists{
                margin: 20px
            }
        }
    }
    .container{
        width: 100%;
        height: 100%;
        margin: 0 auto;
        padding: 50px 0 50px 0;
        display: flex;
        flex-flow: column wrap;
        align-content: flex-start;
    }



</style>