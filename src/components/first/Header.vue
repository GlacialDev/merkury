<template lang="pug">
  div.header
    div.logo.header_logo
      a(href="#").logo_link
        img(src="../../assets/first/logo.png").logo_img
        div.logo_txt Merkury
    div.header_links
      div.nav.header_nav
        ul.nav_list
          each item in [{title: 'Features', link: '#'}, {title: 'Pricing', link: '#'}, {title: 'Blog', link: '#'}, {title: 'Contact', link: '#'}]
            li.nav_item
              a(href=item.link).nav_link #{item.title}
      a(href="#").header_login-btn Login
</template>

<script>
export default {
  name: "Header",
  data() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  flex-direction: row;

  &_links {
    display: flex;
    justify-content: space-between;
    flex-direction: row;
    align-items: center;
  }

  &_login-btn {
    transition: 0.3s;
    text-align: center;
    display: inline-block;
    padding: 16px 44px;
    border: 1px solid #192b56;
    border-radius: 32px;
    color: #5584ff;
    text-decoration: none;
    margin-left: 24px;

    &:hover {
      border: 1px solid #5584ff;      
    }
  }
}

.logo {
  padding: 6vh 20px;

  &_link {
    display: flex;
    flex-direction: row;
    align-items: center;
    text-decoration: none;
  }

  &_img {
    display: inline-block;
    padding-right: 20px;
  }

  &_txt {
    display: inline-block;
    color: #ffffff;
    font-size: 32px;
  }
}

.nav {
  flex-direction: row;

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
    color: #fff;
    text-decoration: none;
    &:hover {
      color: #5584ff;
    }
  }
}
</style>
