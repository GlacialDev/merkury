<template lang="pug">
  div.footer
    div.container
      div.footer_copyright © 2016 Merkury All Right Reserved
      div.nav.footer_nav
        ul.nav_list
          each item in [{title: 'Pricing', link: '#'}, {title: 'Blog', link: '#'}, {title: 'Contact', link: '#'}]
            li.nav_item
              a(href=item.link).nav_link #{item.title}
        ul.nav-icon_list
          li.nav-icon_item
            a(href='#').nav-icon_link
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24px" height="24px">
                <path class="nav-icon_svg" fill="#8492af" d="M17.525,9H14V7c0-1.032,0.084-1.682,1.563-1.682h1.868v-3.18C16.522,2.044,15.608,1.998,14.693,2 C11.98,2,10,3.657,10,6.699V9H7v4l3-0.001V22h4v-9.003l3.066-0.001L17.525,9z"/>
              </svg>
          li.nav-icon_item
            a(href='#').nav-icon_link
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 24 24" version="1.1" width="24px" height="24px">
              <g id="surface1">
              <path class="nav-icon_svg" fill="#8492af" d="M 24 4.300781 C 23.101563 4.699219 22.199219 5 21.199219 5.101563 C 22.199219 4.5 23 3.5 23.398438 2.398438 C 22.398438 3 21.398438 3.398438 20.300781 3.601563 C 19.300781 2.601563 18 2 16.601563 2 C 13.898438 2 11.699219 4.199219 11.699219 6.898438 C 11.699219 7.300781 11.699219 7.699219 11.800781 8 C 7.699219 7.800781 4.101563 5.898438 1.699219 2.898438 C 1.199219 3.601563 1 4.5 1 5.398438 C 1 7.101563 1.898438 8.601563 3.199219 9.5 C 2.398438 9.398438 1.601563 9.199219 1 8.898438 C 1 8.898438 1 8.898438 1 9 C 1 11.398438 2.699219 13.398438 4.898438 13.800781 C 4.5 13.898438 4.101563 14 3.601563 14 C 3.300781 14 3 14 2.699219 13.898438 C 3.300781 15.898438 5.101563 17.300781 7.300781 17.300781 C 5.601563 18.601563 3.5 19.398438 1.199219 19.398438 C 0.800781 19.398438 0.398438 19.398438 0 19.300781 C 2.199219 20.699219 4.800781 21.5 7.5 21.5 C 16.601563 21.5 21.5 14 21.5 7.5 C 21.5 7.300781 21.5 7.101563 21.5 6.898438 C 22.5 6.199219 23.300781 5.300781 24 4.300781 "/>
              </g>
              </svg>
          li.nav-icon_item
            a(href='#').nav-icon_link
              <svg version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 508.52 508.52" style="enable-background:new 0 0 508.52 508.52;" xml:space="preserve">
                <g>
                  <path class="nav-icon_svg" fill="#8492af" d="M277.588,39.442H144.547c-59.624,0-115.752,45.195-115.752,97.54 c0,53.49,40.65,96.682,101.354,96.682l12.332-0.381c-3.941,7.532-6.77,16.018-6.77,24.854c0,14.874,8.009,26.92,18.116,36.741 l-23.074,0.254C56.859,295.1,0,342.202,0,390.956c0,48.087,62.357,78.121,136.22,78.121c84.224,0,130.753-47.801,130.753-95.856 c0-38.52-11.378-61.626-46.53-86.48c-12.014-8.518-35.024-29.208-35.024-41.381c0-14.27,4.068-21.294,25.553-38.075 c21.993-17.194,37.567-41.381,37.567-69.477c0-33.467-14.906-66.108-42.906-76.85h42.175L277.588,39.442z M231.154,364.958 c1.049,4.45,1.621,8.994,1.621,13.73c0,38.87-25.013,69.19-96.809,69.19c-51.074,0-87.942-32.323-87.942-71.161 c0-38.044,45.735-69.699,96.809-69.19c11.918,0.159,23.042,2.034,33.117,5.308C205.664,332.063,225.56,342.965,231.154,364.958z M149.378,220.094c-34.293-1.017-66.87-38.361-72.782-83.365c-5.912-45.036,17.067-79.488,51.329-78.471 c34.262,1.017,66.87,37.154,72.782,82.158C206.65,185.451,183.639,221.111,149.378,220.094z"/>
                  <polygon class="nav-icon_svg" fill="#8492af" points="413.172,133.741 413.172,39.442 381.39,39.442 381.39,133.741 286.042,133.741 286.042,165.523 381.39,165.523 381.39,261.919 413.172,261.919 413.172,165.523 508.52,165.523 508.52,133.741 			"/>
                </g>
              </svg>
</template>

<script>
export default {
	name: 'Footer',
	components: {},
	data() {
		return {};
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.container {
	width: 85%;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
  padding: 0px 95px;
}

.footer {
	display: flex;
	justify-content: center;
	width: 100%;
	background-color: #0e1a35;

	&_copyright {
		font-weight: 300;
		font-size: 18px;
		color: #8492af;
    padding-top: 75px;
    padding-bottom: 75px;
	}
}

.nav {
	display: flex;
	flex-direction: row;
  padding-top: 75px;

	&_list {
		list-style-type: none;
		margin: 0;
	}

	&_item {
		display: inline-block;
		padding: 0px 24px;
	}

	&_link {
		font-weight: 300;
		font-size: 18px;
		transition: 0.3s;
		color: #8492af;
		text-decoration: none;
		&:hover {
			color: #fff;
		}
	}

  &-icon {
    &_list {
      display: flex;
      flex-direction: row;
    }

    &_item {
      width: 24px;
      height: 24px;
      margin-right: 16px;
    }

    &_svg {
      transition: 0.3s;
    }

    &_link:hover {
      .nav-icon_svg {
        fill: #fff;
      }
    }
  }
}
</style>
