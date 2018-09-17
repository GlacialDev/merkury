<template lang="pug">
  div.wrapper.wrapper--third
    div.container
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
      div.slider_info-wrapper
        div.slider_info
          div.slider_title Drag & Drop
          div.slider_text Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
          div.slider_text Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
          div.controllers
            a.controller.controller--left 
              <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="36" height="36" viewBox="0 0 16 16" transform='rotate(180)'>
              <path class="controller_svg  controller_svg--left" fill="#a5aec3" d="M8 1c3.9 0 7 3.1 7 7s-3.1 7-7 7-7-3.1-7-7 3.1-7 7-7zM8 0c-4.4 0-8 3.6-8 8s3.6 8 8 8 8-3.6 8-8-3.6-8-8-8v0z"></path>
              <path class="controller_svg  controller_svg--left" fill="#a5aec3" d="M6 4v8l6-4z"></path>
              </svg>
            a.controller.controller--right
              <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="36" height="36" viewBox="0 0 16 16">
              <path class="controller_svg controller_svg--right" fill="#a5aec3" d="M8 1c3.9 0 7 3.1 7 7s-3.1 7-7 7-7-3.1-7-7 3.1-7 7-7zM8 0c-4.4 0-8 3.6-8 8s3.6 8 8 8 8-3.6 8-8-3.6-8-8-8v0z"></path>
              <path class="controller_svg controller_svg--right" fill="#a5aec3" d="M6 4v8l6-4z"></path>
              </svg>
</template>

<script>
import Task from "./Task";

export default {
  name: "Third",
  components: {
    Task
  },
  data() {
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
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.wrapper {
  font-family: "Roboto", sans-serif;
  display: flex;
  justify-content: center;
  width: 100%;
  min-height: 68.2vh;
  background-color: #0e1a35;
  background-image: url("../../assets/first/graph.jpg");
  background-position: center 30%;
  background-repeat: no-repeat;
  background-size: cover;
}

.container {
  width: 85%;
  padding: 30px 0px;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.slider {
  &_image {
    width: 50%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  &_info-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50%;
  }

  &_info {
    width: 62.5%;
  }

  &_title {
    font-weight: 100;
    font-size: 60px;
    color: #fff;
    padding-bottom: 45px;
  }

  &_text {
    font-weight: 300;
    font-size: 18px;
    color: #8492af;
    padding-bottom: 40px;
  }
}

.controller {
  margin-top: 10px;
  
  &_svg {
    transition: 0.3s;
  }
  &:hover {
    .controller_svg {
      fill: #fff;
    }
  }
  &--left {
    margin-right: 20px;
  }
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
