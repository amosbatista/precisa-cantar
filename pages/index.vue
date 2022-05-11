<template>
  <div class="home">
    <page-header :nav-links="links"/>
    <div class="container">
      <div class="container-center home-content">
        <nuxt-content :document="page" />
        <nuxt-content :document="links" />
      </div>
    </div>
    <page-footer />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData ({ $content }) {
    const page = await $content('index').fetch()
    const links = await $content('links').fetch()

    return {
      page, links
    }
  },
  data () {
    return {
      page: '', links: ''
    }
  }
}
</script>

<style>
  .home ul {
    list-style: none;
    padding-left: 0px;
  }
  .home li {
    margin: 0px 0 20px;
  }
  .home h1 {
    margin: 0 0 60px;
  }
  .home-content {
    margin: 30px 0;
  }
</style>
