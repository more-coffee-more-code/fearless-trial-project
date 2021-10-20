<template>
  <button class="button" type="submit" @click="triggerCounterOnParent">Increase Count</button>
</template>
<script>
export default {
  name: 'Button',
  methods: {
    triggerCounterOnParent() {
      this.$emit('clicked', 1)
    }
  },
}
</script>
<style lang="scss">
@import '../assets/global-styles';

.button {
  padding: 10px 20px;
  border: solid 1px $white;
  border-radius: 4px;
  background-color: $dark-violet;
  color: $white;
  max-width: 300px;
  margin: 0 auto;
  transition: .8s all;
  font-size: $base-font-size;

  &:hover {
    cursor: pointer;
    background-color: $white;
    color: $dark-violet;
  }
}
</style>