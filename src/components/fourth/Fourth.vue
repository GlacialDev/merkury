<template lang="pug">
  div.wrapper.wrapper--fourth
    div.container
      div.title Powerfull PSD Template
      div.text
        p Lorem ipмуsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        p Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      ImageBlock
</template>

<script>
import ImageBlock from './ImageBlock';

export default {
	name: 'Fourth',
	components: {
		ImageBlock
	},
	data() {
		return {};
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.wrapper {
	overflow: hidden;
	font-family: 'Roboto', sans-serif;
	display: flex;
	justify-content: center;
	width: 100%;
	height: 100vh;
	background-color: #fff;
}

.container {
	width: 85%;
	display: flex;
	flex-direction: column;
	text-align: center;
}

.text {
	font-weight: 300;
	font-size: 18px;
	color: #8492af;
	padding: 50px 0px;
}

.title {
	text-align: center;
	font-weight: 100;
	font-size: 60px;
	color: #0e1a35;
	margin-top: 100px;
}
</style>
