<template lang="pug">
  div.wrapper
    div.container
      Header
</template>

<script>
import Header from './Header'

export default {
  name: 'First',
  components: {
    Header
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .wrapper {
    font-family: 'Roboto', sans-serif;
    display: flex;
    justify-content: center;
    width: 100%;
    height: 100vh;
    background-color: #0e1a35;
    background-image: url('../../assets/first/graph.jpg');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .container {
    width: 85%;
  }
</style>
