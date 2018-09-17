<template lang="pug">
  div.feature
    div.feature_img(:style="{'backgroundImage': 'url(' + url + ')'}")
    div.feature_name {{name}}
    div.feature_text {{text}}
    a(href="#").feature_btn See more
</template>

<script>
export default {
  name: 'Feature',
  props: ['url', 'name', 'text'],
  data () {
    return {}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .feature {
    display: flex;
    flex-direction: column;
    text-align: center;
    width: 24%;
    margin: 0px 20px 50px 50px;
    
    &_img {
      width: 100px;
      height: 100px;
      align-self: center;
      background-position: center center;
      background-repeat: no-repeat;
      background-size: contain;
    }

    &_name {
      font-weight: 700;
      font-size: 24px;
      color: #0e1a35;
      padding-top: 50px;
    }

    &_text {
      font-weight: 300;
      font-size: 18px;
      color: #a7b1c5;
      padding-top: 30px;
      padding-bottom: 50px;
    }

    &_btn {
      transition: 0.3s;
      text-align: center;
      display: inline-block;
      min-width: 16%;
      padding: 16px 0px;
      border: 1px solid #dadee7;
      border-radius: 32px;
      color: #0e1a35;
      text-decoration: none;
      &:hover {
        border: 1px solid #192b56;      
      }
    }
  }
</style>
