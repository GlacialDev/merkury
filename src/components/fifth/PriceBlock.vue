<template lang="pug">
  div.price-wrapper
    a(href="#").price
      div.price_title {{title}}
      div.price_cost
        span.price_cost.price_cost-dol $
        span.price_cost.price_cost-num {{cost}}
        span.price_cost.price_cost-time /mon
      ul.price_feature-list
        li(v-for="feature in features").price_feature-item
          div( v-if="feature.type === 'plus'" :style="{'backgroundImage': 'url(' + require('../../assets/fourth/plus.png') + ')'}").price_feature-img
          div( v-else-if="feature.type === 'minus'" :style="{'backgroundImage': 'url(' + require('../../assets/fourth/minus.png') + ')'}").price_feature-img
          div {{feature.text}}
</template>

<script>
export default {
	name: 'PriceBlock',
	props: ['title', 'cost', 'features'],
	components: {},
	data() {
		return {};
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.price {
	transition: 0.3s;
	display: flex;
	flex-direction: column;
	align-items: center;
	min-width: 350px;
	max-width: 350px;
	box-shadow: 0 0 50px #d3d3d3;
	margin-bottom: 30px;

	&:hover {
		box-shadow: 0 0 50px #8e8e8e;
	}

	&_title {
		padding-top: 45px;
		padding-bottom: 32px;
		text-transform: uppercase;
		font-weight: 400;
		font-size: 24px;
		color: #0e1a35;
	}

	&_cost {
		font-weight: 700;
		font-size: 72px;
		color: #0e1a35;
		padding-bottom: 43px;

		&-dol {
			font-size: 40px;
		}

		&-time {
			font-weight: 300;
			font-size: 24px;
			color: #8492af;
		}
	}
}

.price_feature {
	&-list {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	&-item {
		display: flex;
		flex-direction: row;
		align-items: center;
		padding-left: 50px;
		padding-right: 50px;
		padding-bottom: 17px;

		&:last-child {
			padding-bottom: 45px;
		}
	}

	&-img {
		min-width: 24px;
		min-height: 24px;
		margin-right: 15px;
	}
}
</style>
