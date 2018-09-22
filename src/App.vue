<template>
  <div id="app">
    <First/>
    <Second/>
    <Third/>
    <Fourth/>
    <Fifth/>
  </div>
</template>

<script>
import 'normalize.css'
import 'animate.css'
// import { WOW } from 'wowjs'
import First from './components/first/First'
import Second from './components/second/Second'
import Third from './components/third/Third'
import Fourth from './components/fourth/Fourth'
import Fifth from './components/fifth/Fifth'
// window.WOW = WOW
const WOW = require('wowjs');

window.wow = new WOW.WOW({
    boxClass:     'wow',      // класс, скрывающий элемент до момента отображения на экране (по умолчанию, wow)
    animateClass: 'animated', // класс для анимации элемента (по умолчанию, animated)
    offset:       100,          // расстояние в пикселях от нижнего края браузера до верхней границы элемента, необходимое для начала анимации (по умолчанию, 0)
    mobile:       true,       // включение/отключение WOW.js на мобильных устройствах (по умолчанию, включено)
    live:         true,       // поддержка асинхронно загруженных элементов (по умолчанию, включена)
    callback:     function(box) {
      // функция срабатывает каждый раз при старте анимации
      // аргумент box — элемент, для которого была запущена анимация
    },
    scrollContainer: null // селектор прокручивающегося контейнера (опционально, по умолчанию, window)
  
});

window.wow.init();

export default {
  name: 'App',
  components: {
    First,
    Second,
    Third,
    Fourth,
    Fifth
  }
}
</script>

<style lang='scss'>
@import './components/mixins.scss';

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
  font-size: 16px;

  @include w1366_h768 {
    font-size: 13px;
  }
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
