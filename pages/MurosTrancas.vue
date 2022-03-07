<template>
  <div id="page">
    <page-header />
    <nuxt-content :document="page" />
    <page-footer />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('pages/muros-trancas').fetch()

    return {
      page
    }
  }
}
</script>

<style>

</style>
