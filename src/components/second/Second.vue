<template lang="pug">
  div.wrapper.wrapper--second
    div.container
      div.features-wrapper
        Feature(
          v-for="feature in features" :key="feature.key"
          v-bind:url="feature.url"
          v-bind:name="feature.name"
          v-bind:text="feature.text"
        )
      div.requires
        div.requires_title All You need is browser
        div.requires_text Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
        div.requires_text Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisiut aliquip ex ea commodo consequat.  
        ul.requires_list
          li.requires_item 
            div.requires_item-icon
            div.requires_item-text Lorem ipsum dolor sit amet consectetur
          li.requires_item 
            div.requires_item-icon
            div.requires_item-text Ut enim ad minim veniam quis nostrud
    div.planshet
      img(src='../../assets/second/planshet.png').planshet_image
</template>

<script>
import Feature from "./Feature";

export default {
  name: "Second",
  components: {
    Feature
  },
  data() {
    return {
      features: [
        {
          key: 1,
          url: require("./../../assets/second/logo_1.png"),
          name: "Manage Your Workflow",
          text:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur est itaque at eum assumenda aut. Hic voluptates dignissimos officia nam?"
        },
        {
          key: 2,
          url: require("./../../assets/second/logo_2.png"),
          name: "Analytics & Insights",
          text:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur est itaque at eum assumenda aut. Hic voluptates dignissimos officia nam?"
        },
        {
          key: 3,
          url: require("./../../assets/second/logo_3.png"),
          name: "Organize Your Deadlines",
          text:
            " Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur est itaque at eum assumenda aut. Hic voluptates dignissimos officia nam?"
        },
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
  min-height: 100vh;
  background-color: #fff;
  position: relative;
}

.container {
  width: 85%;
  display: flex;
  flex-direction: column;
}

.features-wrapper {
  padding: 200px 0px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}

.requires {
  width: 42%;
  padding-left: 6.5%;
  padding-bottom: 200px;

  &_title {
    font-weight: 100;
    font-size: 60px;
    color: #0e1a35;
    padding-bottom: 60px;
  }

  &_text {
    font-weight: 300;
    font-size: 18px;
    color: #8492af;
    padding-bottom: 40px;
    padding-right: 13.5%;
  }

  &_item {
    display: flex;
    align-items: center;
    font-weight: 300;
    font-size: 22px;
    color: #5584ff;
    padding-top: 15px;
    padding-bottom: 15px;
    padding-right: 13.5%;

    &-icon {
      margin-right: 20px;
      min-width: 30px;
      min-height: 30px;
      background-image: url('../../assets/second/check.png');
    }
  }
}

.planshet {
  width: 50%;
  position: absolute;
  padding-bottom: 100px;
  bottom: 0%;
  right: 0%;
}
</style>
