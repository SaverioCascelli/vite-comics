 <script>

  import novelCard from './novelCard.vue';
  import dcComics from '../data/dc-comics.js';

    export default {
      name: 'AppMain',
      components: { 
        novelCard ,
      },
    data(){
      return{
        dcComics,
      }
    }
}
    </script>

<template>
  <div class="wrapper">
    <div class="container">
      <div class="series">
        <p>current series</p>
      </div>
      <div class="novel-container">
        <novelCard
        v-for="(novel, index) in dcComics"
        :key="index"
        :imgSrc="novel.thumb"
        :serie="novel.series"
        />
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>

@use '../styles/general.scss' as *;
  .wrapper{
    width: 100%;
    background-color: #1c1c1c;
    .container{
      position: relative;
      .series{
        background-color:#0282f9;
        position:absolute;
        padding: 0 20px;
        height: 50px;
        top: -25px;
        left: -25px;
        color: white;
        line-height: 50px;
        text-align: center;
        font-weight: 600;
        font-size: 1.2rem;
        text-transform: uppercase;
            }
      .novel-container{
        display: flex;
        color: white;
        flex-flow: row wrap;
        padding: 50px 0;
        justify-content: flex-start;
        row-gap: 50px;
        column-gap: calc((100% - 190px * 6) / 5);
      }
    }
  }

</style>