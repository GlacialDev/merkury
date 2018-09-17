<template lang="pug">
  div.central
    h1.central_slogan Grow Your business with Merkury
    h4.central_slogan-below Your partner in crime!
    div.central_btn
        a(href="#").central_start-btn Get started
    div.central_img-wrapper
      img(src="../../assets/first/central.jpg").central_img
</template>
        
        
<script>
export default {
  name: "Central",
  data() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.central {
  padding-top: 65px;
  display: flex;
  flex-direction: column;
  position: relative;
  flex-grow: 1;

  &_slogan {
    text-align: center;
    font-size: 60px;
    font-weight: 100;
    color: #fff;
  }

  &_slogan-below {
    text-align: center;
    font-weight: 300;
    font-size: 36px;
    color: #8492af;
  }

  &_btn {
    text-align: center;
    padding-top: 90px;
    padding-bottom: 100px;
  }

  &_start-btn {
    transition: 0.3s;
    display: inline-block;
    text-align: center;
    font-weight: 700;
    color: #fff;
    padding: 14px 56px;
    background-color: #5584ff;
    border-radius: 28px;
    &:hover {
      background-color: #264592;
    }
  }

  &_img-wrapper {
    text-align: center;
    flex-grow: 1;
    position: relative; 
    &:after {
      content: " ";
      position: absolute;
      right: 24%;
      z-index: 1;
      display: inline-block;
      width: 52%;
      height: 100%;
      box-shadow:0 0 80px #274790;
      opacity: 0.46;

    }
  }

  &_img {
    position: absolute;
    right: 24%;
    z-index: 10;
    display: inline-block;
    width: 52%;
  }
}
</style>
