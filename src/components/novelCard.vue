
<script>
export default {
    name:'novelCard',
    props:{
        serie:String,
        imgSrc:String,
    }
}

</script>


<template>
  <div class="novel-card">
    <div class="card-img">
        <img :src="imgSrc" :alt="serie">
    </div>
    <div class="card-title">
        <p>{{serie}}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.novel-card{
        width: 190px;   
        text-transform: uppercase;
        .card-img{
            overflow: hidden;
            aspect-ratio: 1 / 1;
            margin-bottom: 15px;
        }
    }

</style>