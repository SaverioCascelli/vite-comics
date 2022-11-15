    <script>
    export default {
        name: 'AppHeader',
        data(){
          return{
          menu:[
            {
              text:"characters",
              ref:"@",
              current:false
            },
            {
              text:"comics",
              ref:"@",
              current:false
            }, 
            {
              text:"movies",
              ref:"@",
              current:false
            },
            {
              text:"tv",
              ref:"@",
              current:false
            },
            {
              text:"games",
              ref:"@",
              current:false
            },
            {
              text:"videos",
              ref:"@",
              current:true
            }, 
            {
              text:"fans",
              ref:"@",
              current:false
            },
            {
              text:"news",
              ref:"@",
              current:false
            },
            {
              text:"shop",
              ref:"@",
              current:false
            },
          ]
        }
      }
    }
    </script>

<template>
  <header>
    <div class="logo">
      <img src="/dc-logo.png" alt="">
    </div>
    <ul>
      <li
      v-for="(link,index) in menu"
      :key="index"
      :class="{'active':link.current}">
        <a :href="link.ref">{{link.text}}</a>
      </li>
    </ul>
  </header>
</template>


<style lang="scss" scoped>
  @use '../styles/partials/mixin' as *;
  @use '../styles/partials/variables' as *;

  header{
    @include centerFlex('vertical');
    justify-content: space-between;
    height: 200px;
    width: 100%;
    ul{
      @include navListNoStyle('horizontal');
      height: 100%;
      li{
        @include centerFlex();
        height: 100%;
        border-bottom: 5px solid rgba(0,0,0,0);
        &:hover,
        &.active{
          border-bottom: 5px solid $primary-color;
        }
      
    }
    a{
      color: #5b5f5e;
      font-weight: bold;
      text-transform: uppercase;
    }
    }
  }

</style>