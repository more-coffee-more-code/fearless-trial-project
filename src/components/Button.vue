<template>
  <button class="button" type="submit">Increase Count</button>
</template>
<script>
export default {
  name: 'Button'
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
}
</style>