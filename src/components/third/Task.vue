<template lang="pug">
  div.task
    div.task_letter-icon
      div.task_letter {{letter}}
    div.task_description
      div.task_title {{title}}
      div.task_info
        div( v-if="state === 'WiP'" :style="{'backgroundImage': 'url(' + require('../../assets/third/WiP.png') + ')'}").task_state-img
        div( v-else-if="state === 'done'" :style="{'backgroundImage': 'url(' + require('../../assets/third/done.png') + ')'}").task_state-img
        div( v-else-if="state === 'late'" :style="{'backgroundImage': 'url(' + require('../../assets/third/late.png') + ')'}").task_state-img
        div( v-if="state === 'WiP'" :style="{'color': '#aab3c6'}").task_state-time {{timeLeft}}
        div( v-else-if="state === 'done'" :style="{'color': '#42c84f'}").task_state-time {{timeLeft}}
        div( v-else-if="state === 'late'" :style="{'color': '#f85086'}").task_state-time {{timeLeft}}
    a(href="#").task_more-info
</template>

<script>
export default {
  name: "Task",
  props: ["title", "timeLeft", "state"],
  computed: {
    letter: function() {
      return this.title.split("")[0];
    }
  },
  data() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import '../mixins.scss';

.task {
  display: flex;
  flex-direction: row;
  align-items: center;
  color: #0e1a35;
  background-color: #fff;
  width: 100%;
  min-height: rem(100px);
  border: rem(1px) solid #414f70;
  padding-right: rem(30px);
  padding-left: rem(30px);

  &_letter-icon {
    max-width: rem(40px);
    min-width: rem(40px);
    min-height: rem(40px);
    max-height: rem(40px);
    text-align: center;
    background-color: #5584ff;
    border-radius: 50%;
    color: #fff;
  }

  &_letter {
    font-size: rem(23px);
    padding: rem(7px) rem(0px);
  }

  &_description {
    margin-left: rem(20px);
    flex-grow: 1;
  }

  &_title {
    font-size: rem(18px);
    font-weight: 400;
    color: #0e1a35;
  }

  &_info {
    display: flex;
    flex-direction: row;
    margin-top: rem(9px);
  }

  &_state-img {
    min-height: rem(15px);
    min-width: rem(15px);
    margin-right: rem(7px);
    background-repeat: no-repeat;
    background-size: contain;
  }

  &_state-time {
    font-size: rem(14px);
    font-weight: 300;
  }

  &_more-info {
    display: block;
    margin-left: rem(30px);
    border: rem(4px) solid #8492af;
    border-radius: 50%;
    position: relative;
    background-color: currentColor;
    &:before {
      content: "";
      position: absolute;
      border: rem(4px) solid #8492af;
      border-radius: 50%;
      top:rem(-12px);
      margin: rem(-4px);
      background-color: currentColor;
    }
    &:after {
      content: "";
      position: absolute;
      border: rem(4px) solid #8492af;
      border-radius: 50%;
      top: rem(12px);
      margin: rem(-4px);
      background-color: currentColor;
    }
  }
}
</style>
