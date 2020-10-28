<template>
<div class="sample">
  <div>
    <h1>{{ title }}</h1>
    <button
    type="button"
    name="button"
    @click="plus">
    {{ num}}
    </button>
  </div>
  <div :class="['hide', { seven: num === 7}]">
    click 7 times
  </div>
  <div class="slot">
    <slot />
  </div>
</div>


</template>

<script>
export default {
  data() {
    return {
      name: 'takenori',
      num: 0
    }
  },
  props: {
    title: {
      type: String,
      default: 'Default title'
    }
  },
  methods: {
    plus() {
      this.num++
    }
  },
  computed: {
    reverse() {
    }
  },
  mounted() {
    console.log('mounted')
  }
}
</script>

<style lang="css">

</style>