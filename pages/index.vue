<template>
  <div class="home">
    <page-header />
    <div class="center">
      <nuxt-content :document="page" />
    </div>
    <page-footer />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData ({ $content }) {
    const page = await $content('index').fetch()

    return {
      page
    }
  }
}
</script>

<style>
  .center {
    padding: 40px 0 65px;
  }
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
</style>
