    <script>
    export default {
        name: 'AppHeader'
    }
    </script>

<template>
  <header>
    <div class="logo">
      <img src="/dc-logo.png" alt="">
    </div>
    <ul>
      <li>
        <a href="@"> characters</a>
      </li>
      <li>
        <a href="@"> comics</a>
      </li>
      <li>
        <a href="@"> movies</a>
      </li>
      <li>
        <a href="@"> tv</a>
      </li>
      <li>
        <a href="@">games</a>
      </li>
      <li>
        <a href="@">collectables</a>
      </li>
      <li>
        <a href="@">videos</a>
      </li>
      <li>
        <a href="@">fans</a>
      </li>
      <li>
        <a href="@">news</a>
      </li>
      <li>
        <a href="@">shop</a>
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
        &:hover{
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