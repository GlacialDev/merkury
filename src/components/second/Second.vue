<template lang="pug">
  div.wrapper.wrapper--second
    div.container
      div.features-wrapper.fadeInRight.wow
        Feature(
          v-for="feature in features" :key="feature.key"
          v-bind:url="feature.url"
          v-bind:name="feature.name"
          v-bind:text="feature.text"
        )
      div.requires.rollIn.wow
        div.requires_title All You need is a browser!
        div.requires_text Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
        div.requires_text Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisiut aliquip ex ea commodo consequat.  
        ul.requires_list
          li.requires_item 
            div.requires_item-icon
            div.requires_item-text Lorem ipsum dolor sit amet consectetur
          li.requires_item 
            div.requires_item-icon
            div.requires_item-text Ut enim ad minim veniam quis nostrud
    div.planshet.bounceInRight.wow
      img(src='../../assets/second/planshet.png').planshet_image
</template>

<script>
import Feature from './Feature';

export default {
	name: 'Second',
	components: {
		Feature
	},
	data() {
		return {
			features: [
				{
					key: 1,
					url: require('./../../assets/second/logo_1.png'),
					name: 'Manage Your Workflow',
					text:
						' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur est itaque at eum assumenda aut. Hic voluptates dignissimos officia nam?'
				},
				{
					key: 2,
					url: require('./../../assets/second/logo_2.png'),
					name: 'Analytics & Insights',
					text:
						' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur est itaque at eum assumenda aut. Hic voluptates dignissimos officia nam?'
				},
				{
					key: 3,
					url: require('./../../assets/second/logo_3.png'),
					name: 'Organize Your Deadlines',
					text:
						' Lorem ipsum dolor sit, amet consectetur adipisicing elit. Tenetur est itaque at eum assumenda aut. Hic voluptates dignissimos officia nam?'
				}
			]
		};
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
	padding: rem(250px) rem(190px) rem(260px) rem(190px);
	display: flex;
	flex-direction: row;
	flex-wrap: wrap;
	justify-content: space-between;

    @include w1366_h768 {
			padding: rem(250px) rem(50px) rem(160px) rem(50px);
		}
		
    @include w1024_h768 {
			padding: rem(160px) rem(50px) rem(120px) rem(50px);
    }

    @include w1280_h800 {
			padding: rem(250px) rem(0px) rem(60px) rem(0px);
    }

    @include w1024_h768 {
			padding: rem(160px) rem(0px) rem(60px) rem(0px);
    }
}

.requires {
	width: 45%;
	padding-left: 6.5%;
	padding-bottom: rem(270px);

	@include w1280_h800 {
		padding-bottom: rem(130px);
	}

	@include w1024_h768 {
		padding-bottom: rem(270px);
	}

	&_title {
		font-weight: 100;
		font-size: rem(60px);
		color: #0e1a35;
		padding-bottom: rem(60px);
		
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
		padding-right: 13.5%;
	}

	&_item {
		display: flex;
		align-items: center;
		font-weight: 300;
		font-size: rem(22px);
		color: #5584ff;
		padding-top: rem(15px);
		padding-bottom: rem(15px);
		padding-right: 13.5%;

		&-icon {
			margin-right: rem(20px);
			min-width: rem(30px);
			min-height: rem(30px);
			background-image: url('../../assets/second/check.png');
			background-size: contain;
		}
	}
}

.planshet {
	width: 51%;
	position: absolute;
	padding-bottom: rem(120px);
	bottom: 0%;
	right: 0%;
	
	@include w1366_h768 {
		padding-bottom: rem(40px);
	}

	@include w1280_h800 {
		padding-bottom: rem(40px);
	}
}
</style>
