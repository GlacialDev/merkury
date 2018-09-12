<template lang="pug">
  div.header
    div.logo.header_logo
      img(src="../../assets/first/logo.png").logo_img
      div.logo_txt Mercury
    div.header_links
      div.nav.header_nav
        ul.nav_list
          each item in ['Features', 'Pricing', 'Blog', 'Contact']
            li.nav_item
              a(link="#").nav_link #{item}
      div.header_login-btn
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
}

.logo {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.logo_img {
  display: inline-block;
  padding: 6vh 20px;
}

.logo_txt {
  display: inline-block;
  color: #ffffff;
  font-size: 32px;
}

.header_links {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: center;
}

.nav {
  flex-direction: row;
}

.nav_list {
  list-style-type: none;
  margin: 0;
}

.nav_item {
  display: inline-block;
  color: #fff;
  padding: 0px 24px;
}
</style>
