<template>
  <div id="page">
    <Header />
    <Menu />
    <nuxt-content :document="page" />
    <Footer />
  </div>
</template>

<script>
  export default {
    async asyncData ({ $content }) {
      const page = await $content('pages/carnaval-que-horror').fetch()

      return {
        page
      }
    }
  }
</script>

<style>

</style>