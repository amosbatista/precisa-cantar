<template>
  <div id="page">
    <page-header :nav-links="links"/>
    <div class="container">
      <div class="container-center page-content">
        <nuxt-content :document="page" />
      </div>
    </div>
    <page-footer />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('pages/sobre').fetch()
    const links = await $content('links').fetch()

    return {
      page, links
    }
  }
}
</script>

<style>

</style>
