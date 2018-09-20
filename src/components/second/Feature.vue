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
@import '../mixins.scss';

  .feature {
    display: flex;
    flex-direction: column;
    text-align: center;
    width: 25%;
    padding-bottom: rem(20px);
    position: relative;

    &:after {
      content: ' ';
      position: absolute;
      border: rem(1px) solid #dadee7;
      width: 70%;
      top: 12%;
      right: -60%;
    }

    &:nth-of-type(3) {
      &:after {
        content: none;
      }
    }
    
    &_img {
      width: rem(100px);
      height: rem(100px);
      align-self: center;
      background-position: center center;
      background-repeat: no-repeat;
      background-size: contain;
    }

    &_name {
      font-weight: 700;
      font-size: rem(24px);
      color: #0e1a35;
      padding-top: rem(50px);
    }

    &_text {
      font-weight: 300;
      font-size: rem(18px);
      color: #a7b1c5;
      padding-top: rem(30px);
      padding-bottom: rem(50px);
    }

    &_btn {
      transition: 0.3s;
      text-align: center;
      display: inline-block;
      min-width: 16%;
      padding: rem(16px) rem(0px);
      border: rem(1px) solid #dadee7;
      border-radius: rem(32px);
      color: #0e1a35;
      text-decoration: none;
      &:hover {
        border: rem(1px) solid #192b56;      
      }
    }
  }
</style>
