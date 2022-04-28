<template>
  <div id="page">
    <page-header />
    <div class="container">
      <div class="container-center page-content poetry">
        <nuxt-content :document="page" />
      </div>
    </div>
    <page-footer />
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('pages/cordel').fetch()

    return {
      page
    }
  }
}
</script>

<style>

</style>
