
<script>
import { stringifyExpression } from '@vue/compiler-core';

export default {
    name:'VerticalList',
    props:{
        listObj: Object,
    }
}
</script>
<template>
    <div>
        <h3>{{listObj.title}}</h3>
        <ul>
            <li 
            v-for="(link, index) in listObj.links" 
            :key="index">
            {{link}}
            </li>
        </ul>
    </div>
</template>


<style lang="scss" scoped>

    h3{
        color: white;
        text-transform: uppercase;
        margin-bottom: 20px;
    }
    ul{
        color: grey;
        font-size: .9rem;
        text-transform: capitalize;
        list-style: none;
        li{
            margin-top: 3px;
        }
    }

</style>