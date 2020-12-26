<template>
  <div>
    <sample :title="indextitle">
      <div class="come">slot example</div>
    </sample>
    <nuxt-link to="/about">ABOUT</nuxt-link>
  </div>
</template>

<script>
import Sample from '@/components/Sample.vue'

export default {
  components: {
    Sample,
  },
  data() {
    return {
      indextitle: 'Nuxt.js data',
    }
  },
}
</script>

<style></style>
