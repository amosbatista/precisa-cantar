<template>
  <nav class="container">
    <div class="container-center links">
      <a
        v-for="link, linkIndex in links"
        :key="linkIndex"
        :href="link.sub ? '#' : link.url"
        v-on:click="openMenu(linkIndex)"
        class="link">
        <div
          class="sub-menu"
          v-if="link.isOpened && link.sub">
          <a
            v-for="subLink, subLinkIndex in link.sub"
            :key="subLinkIndex"
            :href="subLink.url"
          >
            {{ subLink.text }}
          </a>
        </div>
        <div
          class="icon"
          v-if="link.sub">
          &#8964;
        </div>
        {{ link.text }}
      </a>
    </div>
  </nav>
</template>

<script>
import links from './linkList'
export default {
  name: 'PageMenu',
  props: ['navLinks'],
  methods: {
    openMenu (clikedLinkIndex) {
      this.links = this.links.map((link, linkIndex) => {
        return {
          ...link,
          isOpened: linkIndex === clikedLinkIndex
        }
      })
    }
  },
  data () {
    return {
      links: links.map((link) => {
        return {
          ...link,
          isOpened: false
        }
      })
    }
  }
}
</script>

<style>
  nav {
    background-color: #41237b;
  }
  .links {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    flex-wrap: wrap;
    list-style: none;
    padding-left: 0px;
  }
  .link {
    margin: 0 0 0 10px;
    height: 50px;
  }
  nav li {
    margin: 0 0 0 10px;
  }
  nav a, nav span {
    color: #efe0b3;
    font-size: 75%;
    margin: 0;
  }
  nav a {
    padding: 0 8px;
    display: flex;
    flex-direction: row;
    align-items: center;
    text-decoration: none;
    position: relative;
  }
  nav .icon {
    font-size: 150%;
    height: 45px;
    margin-right: 3px;
  }
  .sub-menu {
    position: absolute;
    background-color: rgb(5, 16, 30);
    height: auto;
    top: 40px;
    left: 30px;
    display: flex;
    padding: 10px 3px;
    z-index: 2;
  }
</style>
