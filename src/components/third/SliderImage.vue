<template lang="pug">
  div.slider_image
    div.column.column--left
      div.column_title
        div.column_name In Progress 
          span.column_name-num ({{ tasks_left.length }})
        img(src="../../assets/third/arrow.png").column_name-arrow
      ul.task_list.task_list--left
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
      ul.task_list.task_list--right
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
  padding-bottom: 15px;
}

.column {
  width: 50%;
  display: flex;
  flex-direction: column;

  &--right {
    padding-left: 15px;
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

.task_list {
  &--left{
    margin-right: 40px;
  }
  &--right {
    margin-right: 20px;
  }
}

.task_item {
  margin-bottom: 12px;

  &--left:nth-of-type(3) {
    position: relative;
    margin-top: 30px;
    margin-left: 28px;

    &::after {
      position: absolute;
      content: " ";
      top: 52%;
      left: 87.5%;
      width: 5vw;
      height: 5vw;
      background-color: rgba(132, 146, 175, 0.2);
      background-image: url("../../assets/third/hand.png");
      background-position: center center;
      background-repeat: no-repeat;
      background-size: 50%;
      border-radius: 50%;
    }

    &::before {
      position: absolute;
      content: " ";
      top: 60%;
      left: 90%;
      width: 4vw;
      height: 4vw;
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
  width: 100%;
  min-height: 100px;
  border: 3px dashed #3d4966;

  &-text {
    font-size: 20px;
    font-weight: 400;
    color: #8492af;
  }
}
</style>
