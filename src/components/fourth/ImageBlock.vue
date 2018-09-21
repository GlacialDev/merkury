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
@import '../mixins.scss';

  .image-wrapper {
    width: 100%;
    min-height: 71%;
    background-image: url('../../assets/fourth/aksonometry.png');
    background-position: center center;
    background-repeat: no-repeat;
    background-size: contain;
    position: relative;

    @include w1366_h768 {
      min-height: 60%;
    }

    @include w1280_h800 {
      min-height: 66%;
    }
  }

  .pointer {
    position: absolute;
    top: 0;
    left: 0;

    &--first {
      top: 25%;
      left: 48.7%;
      transform: rotate(180deg);

      .pointer_info {
        top: rem(-60px);
        left: rem(415px);
        text-align: left;
        transform: rotate(180deg);

        @include w1366_h768 {
          left: rem(265px);
        }

        @include w1280_h800 {
          left: rem(265px);
        }
      }
    }

    &--second {
      top: 57%;
      left: 51.7%;

      .pointer_info {
        top: rem(-25px);
        left: rem(415px);
        text-align: right;

        @include w1366_h768 {
          left: rem(265px);
        }

        @include w1280_h800 {
          left: rem(265px);
        }
      }
    }

    &_circle {
      z-index: 10;
      position: absolute;
      top: rem(7.5px);
      left: rem(7.5px);
      width: rem(30px);
      height: rem(30px);
      border-radius: 50%;
      background-color: #5584ff;
    }
    &_circle-big {
      z-index: 1;
      position: absolute;
      top: 0;
      left: 0;
      width: rem(46px);
      height: rem(46px);
      border-radius: 50%;
      background-color: #5584ff;
      opacity: 0.5;
    }

    &_line {
      z-index: 1;
      position: absolute;
      top: rem(21px);
      left: rem(21px);
      border: rem(2px) solid #5584ff;
      width: rem(650px);

      @include w1366_h768 {
        width: rem(500px);
      }

      @include w1280_h800 {
        width: rem(500px);
      }
    }

    &_info {
      position: absolute;
      width: rem(256px);
    }

    &_title {
      color: #0e1a35;
      font-weight: 700;
      font-size: rem(24px);
      padding-bottom: rem(45px);
    }

    &_text {
      color: #8492af;
      font-weight: 300;
      font-size: rem(18px);
    }
  }
</style>
