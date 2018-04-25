<template>
  <div>
    <div class="fitness-wrapper">
      <div class="fitness-item">
        <span>Pushups</span>
        <div
          class="fitness-number"
          :class="fitnessStatus('pushups')"
        >{{ fitness.pushups }}</div>
      </div>
      <div class="fitness-item">
        <span>Situps</span>
        <div
          class="fitness-number"
          :class="fitnessStatus('situps')"
        >{{ fitness.situps }}</div>
      </div>
      <div class="fitness-item">
        <span>Squats</span>
        <div
          class="fitness-number"
          :class="fitnessStatus('squats')"
        >{{ fitness.squats }}</div>
      </div>
      <div class="fitness-item">
        <span>Calf Raises</span>
        <div
          class="fitness-number"
          :class="fitnessStatus('calfRaises')"
        >{{ fitness.calfRaises }}</div>
      </div>
    </div>

    <div
      class="food-wrapper"
      v-if="food.log"
    >
      <div class="food-label">Food Log</div>
      <div class="food-log">{{ food.log }}</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'overview',
    props: [
      'food',
      'fitness'
    ],
    methods: {
      // Sends back a class if there are numbers in there.
      fitnessStatus (exercise) {
        if (this.fitness[exercise] > 0) {
          return 'active'
        }
      }
    },
    data () {
      return {
        status: ''
      }
    }
  }
</script>

<style scoped>
  .fitness-wrapper {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .fitness-item,
  .food-wrapper {
    padding-left: 0.5rem;
    padding-right: 0.5rem;
  }

  .fitness-item {
    margin-bottom: 2rem;
    text-align: center;
    width: 45%;
  }

  .fitness-number {
    color: #AA0000;
    font-size: 5rem;
  }

  .fitness-number.active {
    color: #008000;
  }

  .food-wrapper {
    padding-top: 2rem;
  }

  .food-label {
    text-align: center;
  }

  .food-log {
    border: 1px solid #ccc;
    margin-top: 1rem;
    padding: 2rem;
  }

</style>
