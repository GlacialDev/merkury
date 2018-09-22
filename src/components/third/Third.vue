<template lang="pug">
  div.wrapper.wrapper--third
    div.container
      SliderImage.fadeInDown.wow
      div.slider_info-wrapper.fadeInUp.wow
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
import SliderImage from './SliderImage';

export default {
	name: 'Third',
	components: {
		SliderImage
	},
	data() {
		return {};
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import '../mixins.scss';

.wrapper {
  overflow: hidden;
	font-family: 'Roboto', sans-serif;
	display: flex;
	justify-content: center;
	width: 100%;
	min-height: 68.2vh;
	background-color: #0e1a35;
	background-image: url('../../assets/first/graph.jpg');
	background-position: center 30%;
	background-repeat: no-repeat;
	background-size: cover;
}

.container {
	width: 85%;
	padding: rem(30px) rem(0px);
	display: flex;
	flex-direction: row;
	align-items: center;
}

.slider {
	&_info-wrapper {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 50%;

    @include w1366_h768 {
			width: 40%;
    }

		@include w1280_h800 {
			width: 40%;
		}
	}

	&_info {
		width: 62.5%;
		padding-bottom: rem(15px);
		
    @include w1366_h768 {
			width: 75%;
    }

		@include w1280_h800 {
			width: 75%;
		}
	}

	&_title {
		font-weight: 100;
		font-size: rem(60px);
		color: #fff;
		padding-bottom: rem(45px);

    @include w1366_h768 {
			font-size: rem(45px);
    }

		@include w1280_h800 {
			font-size: rem(45px);
		}
	}

	&_text {
		font-weight: 300;
		font-size: rem(18px);
		color: #8492af;
		padding-bottom: rem(40px);
	}
}

.controller {
	margin-top: rem(10px);

	&_svg {
		transition: 0.3s;
	}
	&:hover {
		.controller_svg {
			fill: #fff;
		}
	}
	&--left {
		margin-right: rem(20px);
	}
}
</style>
