<template>
  <div class="display">
    <div class="display__wrapper">
      <p class="number-display" v-if="displayCount === true">{{ currentCount }}</p>
      <p class="number-display" v-if="displayHits === true">{{ displayHits }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'NumberDisplay',
  props: {
    currentCount: Number,
    totalHits: Number,
    displayCount: Boolean,
    displayHits: Boolean
  },
  methods: {
  
  }
}
</script>
<style lang="scss">
.display {
  &__wrapper {

  }

  &__number {

  }
}
</style>