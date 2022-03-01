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
  name: 'IndexPage',
  async asyncData ({ $content }) {
    const page = await $content('index').fetch()

    return {
      page
    }
  }
}
</script>
