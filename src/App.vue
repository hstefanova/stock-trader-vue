<template>
  <div id="app">
    <Header></Header>

    <Main></Main>
  </div>
</template>

<script>
import Header from './components/Header'
import Main from './components/Main'

export default {
  components: {
    Header,
    Main
  }
}
</script>

<style lang="scss">
  * { margin: 0; padding: 0; box-sizing: border-box; }
  // Main Navigation
  .nav {
    display: flex;
    align-items: center; 

    > li {
      & + li {
        margin: 0 10px;
      }
    }
  }

  // Nav Utilities
  .nav--utilities {
    li {
      position: relative;
    }

    .nav__dropdown {
      position: absolute;
      top:100%;
      left:0;
    }
  }

  //Buttons
  
</style>