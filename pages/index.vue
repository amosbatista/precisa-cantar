<template>
  <div id="page">
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
  #page ul {
    list-style: none;
    padding-left: 10px;
  }
  #page li {
    margin: 0px 0 30px;
  }
</style>
