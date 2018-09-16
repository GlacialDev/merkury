<template lang="pug">
  div.wrapper.wrapper--first
    div.container
      Header
      Central
</template>

<script>
import Header from './Header'
import Central from './Central'

export default {
  name: 'First',
  components: {
    Header,
    Central
  },
  data () {
    return {}
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
    display: flex;
    flex-direction: column;
  }
</style>
