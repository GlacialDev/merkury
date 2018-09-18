<template lang="pug">
  div.slider_image
    div.column.column--left
      div.column_title
        div.column_name In Progress 
          span.column_name-num ({{ tasks_left.length }})
        img(src="../../assets/third/arrow.png").column_name-arrow
      ul.task_list
        Task(
          v-for = "task in tasks_left" :key="task.key"
          v-bind:title="task.title"
          v-bind:timeLeft="task.timeLeft"
          v-bind:state="task.state"
        ).task_item.task_item--left
    div.column.column--right
      div.column_title
        div.column_name Completed 
          span.column_name-num ({{ tasks_right.length }})
      Task(
        v-for = "task in tasks_right" :key="task.key"
        v-bind:title="task.title"
        v-bind:timeLeft="task.timeLeft"
        v-bind:state="task.state"
      ).task_item.task_item--right
      div.task_drop
        div.task_drop-text Drop here
</template>

<script>
import Task from './Task'

export default {
  name: 'SliderImage',
  components: {
    Task
  },
  data () {
    return {
      tasks_left: [
        {
          key: 1,
          title: "New logo for Apple",
          timeLeft: "1 day left",
          state: "WiP"
        },
        {
          key: 2,
          title: "Daily UI Kit",
          timeLeft: "5 days left",
          state: "WiP"
        },
        {
          key: 3,
          title: "Business Cards",
          timeLeft: "2 days delays",
          state: "late"
        }
      ],
      tasks_right: [
        {
          key: 1,
          title: "Free PSD Template vol. 1",
          timeLeft: "Completed!",
          state: "done"
        },
        {
          key: 2,
          title: "Iconset vol. 1",
          timeLeft: "Completed!",
          state: "done"
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.slider_image {
  width: 50%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.column {
  display: flex;
  flex-direction: column;

  &--right {
    margin-right: 24px;
  }

  &_title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-bottom: 32px;
  }

  &_name {
    font-size: 30.5px;
    font-weight: 400;
    color: #fff;

    &-num {
      color: #8492af;
    }

    &-arrow {
      width: 14px;
      height: 25px;
      margin-right: 28px;
      display: inline-block;
    }
  }
}

.task_item {
  margin-bottom: 12px;

  &--left:nth-of-type(3) {
    position: relative;
    margin-top: 24px;
    margin-left: 28px;

    &::after {
      position: absolute;
      content: " ";
      top: 100px - 96px/2;
      left: 390px - 96px/2;
      width: 96px;
      height: 96px;
      background-color: rgba(132, 146, 175, 0.2);
      background-image: url("../../assets/third/hand.png");
      background-position: center center;
      background-repeat: no-repeat;
      border-radius: 50%;
    }

    &::before {
      position: absolute;
      content: " ";
      top: 100px - 76px/2;
      left: 390px - 76px/2;
      width: 76px;
      height: 76px;
      background-color: #8492af;
      border-radius: 50%;
      opacity: 0.2;
    }
  }
}

.task_drop {
  display: flex;
  justify-content: center;
  align-items: center;
  min-width: 390px;
  max-width: 390px;
  min-height: 100px;
  border: 3px dashed #3d4966;

  &-text {
    font-size: 20px;
    font-weight: 400;
    color: #8492af;
  }
}
</style>
