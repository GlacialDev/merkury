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
@import '../mixins.scss';

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
    padding: rem(16px) rem(44px);
    border: rem(1px) solid #192b56;
    border-radius: rem(32px);
    color: #5584ff;
    text-decoration: none;
    margin-left: rem(24px);

    &:hover {
      border: rem(1px) solid #5584ff;      
    }
  }
}

.logo {
  padding: 6vh rem(10px);

  &_link {
    display: flex;
    flex-direction: row;
    align-items: center;
    text-decoration: none;
  }

  &_img {
    display: inline-block;
    padding-right: rem(15px);
  }

  &_txt {
    display: inline-block;
    color: #ffffff;
    font-size: rem(42px);
  }
}

.nav {
  flex-direction: row;

  &_list {
    list-style-type: none;
    margin-bottom: rem(8px);
    margin-right: rem(8px);
  }

  &_item {
    display: inline-block;
    padding: rem(0px) rem(24px);
  }

  &_link {
    font-weight: 300;
    font-size: rem(18px);
    transition: 0.3s;
    color: #fff;
    text-decoration: none;
    &:hover {
      color: #5584ff;
    }
  }
}
</style>
