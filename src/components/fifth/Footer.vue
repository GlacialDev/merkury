<template lang="pug">
  div.footer
    div.container
      div.footer_copyright © 2016 Merkury All Right Reserved
      div.footer_nav

</template>

<script>
export default {
  name: 'Footer',
  components: {
  },
  data () {
    return {}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .container {
    width: 85%;
  }

  .footer {
    display: flex;
    justify-content: center;
    width: 100%;
    background-color: #0e1a35;

    &_copyright {
      font-weight: 300;
      font-size: 18px;
      color: #8492af;
      padding: 60px 0px;
    }
  }
</style>
