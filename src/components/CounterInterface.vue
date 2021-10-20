<template>
  <div class="counter-interface">
    <div class="counter-interface__content">
      <div class="counter-interface__displays">
        <number-display class="counter-interface__display" :currentCount="this.count" :displayCount="true"/>
        <number-display class="counter-interface__display" :totalHits="this.hits" :displayHits="true"/>
      </div>
      <counter-button class="counter-interface___button" @clicked="incrementCount"/>
    </div>
  </div>
</template>
<script>
import CounterButton from '../components/Button.vue'
import NumberDisplay from '../components/NumberDisplay.vue'

export default {
  name: 'CounterInterface',
  components: {
    NumberDisplay,
    CounterButton
  },
  data() {
    return {
      count: 0,
      hits: 0
    }
  },
  watch: {
    count() {
      console.log('count changed')
      this.getDataFromApi()
    }
  },
  methods: {
    incrementCount(value) {
      return this.count += value
    },
    getDataFromApi() {
      fetch("https://api.countapi.xyz/hit/localhost/visits")
      .then(response => response.json())
      .then(data => this.hits = data.value);
    }
  }
}
</script>
<style lang="scss">
@import '../assets/global-styles';

.counter-interface {
  background-color: $dark-violet;
  border: solid 1px $light-violet;
  width: max-content;
  margin: 0 auto;

  &__content {
    display: flex;
    flex-direction: column;
    margin: 70px;
  }

  &__displays {
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-bottom: 40px;
  }

  &__display {
    margin: 0 10px;
  }
}
</style>