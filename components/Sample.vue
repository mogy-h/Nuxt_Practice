<template>
  <div>
    <h1>{{ title }}</h1>
    <h3>Hello, {{ name }}</h3>
    <p>
      {{ reverseName }}
    </p>

    <p :class="['hide', { seven: num === 7 }]">7回クリックしたら表示</p>

    <button type="button" name="button" @click="plus">クリック{{ num }}</button>

    <div class="slot">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default title',
    },
  },
  data() {
    return {
      name: 'mogihiroki',
      num: 0,
    }
  },
  computed: {
    reverseName() {
      return this.name.split('').reverse().join('')
    },
  },
  methods: {
    plus() {
      this.num++
    },
  },
}
</script>

<style lang="scss" scoped>
.hide {
  display: none;
  &.seven {
    display: block;
  }
}
</style>
