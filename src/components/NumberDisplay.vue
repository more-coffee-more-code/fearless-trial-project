<template>
  <div class="display">
    <div class="display__wrapper">
      <p class="display__number display__number--count" v-if="displayCount === true">{{ currentCount }}</p>
      <p class="display__number display__number--hits" v-else-if="displayHits === true">{{ totalHits }}</p>
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
@import '../assets/global-styles';

.display {

  &__number {
    color: $red-orange;
    display: flex;
    flex-direction: column;
    font-size: $large-font-size;
    
    &--hits {
      &:before {
        content: 'Total Hits';
        padding-bottom: 20px;
        font-size: $small-font-size;
        color: $light-violet;
      }
    }

    &--count {
      &:before {
        content: 'Button Clicks';
        padding-bottom: 20px;
        font-size: $small-font-size;
        color: $light-violet;
      }
    }
  }
}
</style>