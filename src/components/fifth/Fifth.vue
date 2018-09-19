<template lang="pug">
  div.wrapper.wrapper--fifth
    div.container
      div.title Check our pricing!
      div.pricing
        PriceBlock(
          v-for='plan in plans' :key='plan.key'
          v-bind:title='plan.title'
          v-bind:cost='plan.cost'
          v-bind:features='plan.features'
        )
      div.text-after Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris.
      div.join
        a(href="#").join-btn Join now!
    Footer
</template>

<script>
import PriceBlock from './PriceBlock';
import Footer from './Footer';

export default {
	name: 'Fifth',
	components: {
		PriceBlock,
		Footer
	},
	data() {
		return {
			plans: [
				{
					key: 1,
					title: 'Bronze plan',
					cost: '19',
					features: [
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'minus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'minus',
							text: 'Lorem ipsum dolor sit am'
						}
					]
				},
				{
					key: 2,
					title: 'Silver plan',
					cost: '49',
					features: [
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'minus',
							text: 'Lorem ipsum dolor sit am'
						}
					]
				},
				{
					key: 3,
					title: 'Gold plan',
					cost: '99',
					features: [
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						},
						{
							type: 'plus',
							text: 'Lorem ipsum dolor sit am'
						}
					]
				}
			]
		};
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.wrapper {
	overflow: hidden;
	font-family: 'Roboto', sans-serif;
	display: flex;
	flex-direction: column;
	align-items: center;
	width: 100%;
}

.container {
	width: 85%;
	display: flex;
	flex-direction: column;
	align-items: center;
}

.title {
	text-align: center;
	font-weight: 100;
	font-size: 60px;
	color: #0e1a35;
	margin-top: 50px;
	margin-bottom: 90px;
}

.pricing {
	display: flex;
	flex-direction: row;
	flex-wrap: wrap;
	justify-content: space-around;
	padding: 0px 105px;
	margin-bottom: 70px;
	width: 100%;
}

.text-after {
	text-align: center;
	width: 55%;
	font-weight: 300;
	font-size: 18px;
	line-height: 30px;
	color: #8492af;
	margin-bottom: 60px;
}

.join {
	text-align: center;
	padding-bottom: 100px;

	&-btn {
		position: relative;
		transition: 0.3s;
		display: inline-block;
		text-align: center;
		font-weight: 700;
		color: #fff;
		padding: 15px 70px;
		background-color: #5584ff;
		border-radius: 28px;
		&:hover {
			background-color: #264592;
		}

	

		&:after {
		content: ' ';
		position: absolute;
		border: 1px solid #dadee7;
		width: 110%;
		top: 50%;
		right: -120%;
		}

		&:before {
		content: ' ';
		position: absolute;
		border: 1px solid #dadee7;
		width: 110%;
		top: 50%;
		left: -120%;
		}
	}
}
</style>
