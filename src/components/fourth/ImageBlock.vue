<template lang="pug">
  div.image-wrapper
    div.pointer.pointer--first
      div.pointer_circle
      div.pointer_circle-big
      div.pointer_line
      div.pointer_info
        div.pointer_title Clean & modern layout
        div.pointer_text Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt 
    div.pointer.pointer--second
      div.pointer_circle
      div.pointer_circle-big
      div.pointer_line
      div.pointer_info
        div.pointer_title Easy to customize
        div.pointer_text Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt 
</template>

<script>

export default {
  name: 'ImageBlock',
  data () {
    return {}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .image-wrapper {
    width: 100%;
    height: 60%;
    background-image: url('../../assets/fourth/aksonometry.png');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: contain;
    position: relative;
  }

  .pointer {
    position: absolute;
    top: 0;
    left: 0;

    &--first {
      top: 25%;
      left: 49%;
      transform: rotate(180deg);

      .pointer_info {
        top: -60px;
        left: 415px;
        text-align: left;
        transform: rotate(180deg);
      }
    }

    &--second {
      top: 63%;
      left: 52.2%;

      .pointer_info {
        top: -25px;
        left: 415px;
        text-align: right;
      }
    }

    &_circle {
      z-index: 10;
      position: absolute;
      top: 7.5px;
      left: 7.5px;
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background-color: #5584ff;
    }
    &_circle-big {
      z-index: 1;
      position: absolute;
      top: 0;
      left: 0;
      width: 46px;
      height: 46px;
      border-radius: 50%;
      background-color: #5584ff;
      opacity: 0.5;
    }

    &_line {
      z-index: 1;
      position: absolute;
      top: 21px;
      left: 21px;
      border: 2px solid #5584ff;
      width: 650px;
    }

    &_info {
      position: absolute;
      width: 256px;
    }

    &_title {
      color: #0e1a35;
      font-weight: 700;
      font-size: 24px;
      padding-bottom: 45px;
    }

    &_text {
      color: #8492af;
      font-weight: 300;
      font-size: 18px;
    }
  }
</style>
