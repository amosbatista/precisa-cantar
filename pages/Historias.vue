<template>
  <div class="historias">
    <page-header />
    <div class="container">
      <div class="container-center historias-content">
        <nuxt-content :document="page" />
      </div>
    </div>
    <page-footer />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData ({ $content }) {
    const page = await $content('historias').fetch()

    return {
      page
    }
  },
  data () {
    return {
      page: ''
    }
  }
}
</script>

<style>
  .historias h3 {
    font-size: 110%;
    margin: 50px 0 20px;
  }
  .historias ul {
    list-style: none;
    padding-left: 0px;
  }
  .historias li {
    margin: 0px 0 20px;
  }
  .historias-content {
    margin: 30px 0 50px;
    min-height: 200px;
  }
</style>
