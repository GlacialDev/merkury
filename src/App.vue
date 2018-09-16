<template>
  <div id="app">
    <First/>
    <Second/>
  </div>
</template>

<script>
import 'normalize.css'
import First from './components/first/First'
import Second from './components/second/Second'

export default {
  name: 'App',
  components: {
    First,
    Second
  }
}
</script>

<style>
@font-face {
  font-family: 'Roboto';
  src: url(./assets/fonts/Roboto-Bold-webfont.woff) format('woff');
  font-weight: 700;
  font-style: normal;
}

@font-face {
  font-family: 'Roboto';
  src: url(./assets/fonts/Roboto-Regular-webfont.woff) format('woff');
  font-weight: 300;
  font-style: normal;
}

@font-face {
  font-family: 'Roboto';
  src: url(./assets/fonts/Roboto-Medium-webfont.woff) format('woff');
  font-weight: 400;
  font-style: normal;
}

@font-face {
  font-family: 'Roboto';
  src: url(./assets/fonts/Roboto-Thin-webfont.woff) format('woff');
  font-weight: 100;
  font-style: normal;
}

* {
	margin: 0;
	padding: 0;
	font: inherit;
}

*, *:before, *:after {
	/*-webkit-box-sizing: border-box;
	-moz-box-sizing: border-box;*/
	box-sizing: border-box;
}

*:focus, *:active, *:hover {
	outline: none;
}

html {
	font-family: sans-serif;
	cursor: default;
	height: 100%;
}

body {
	height: 100%;
	width: 100%;
	overflow-x: hidden;
}

ol, ul, li {
	list-style-type: none;
}

table {
	border-collapse: collapse;
	border-spacing: 0;
}

a {
	text-decoration: none;
	cursor: pointer;
	color: inherit;
	background: transparent;
}

h1, h2, h3 {
	margin: 0;
}
</style>
