<template>
  <div>
    <div class="wrapper">
      <p class="help-text">Keep track of your exercises here!</p>

      <fieldset>
        <label for="pushups">Push-ups</label>

        <input
          type="number"
          name="pushups"
          id="pushups"
          step="10"
          v-model="fitness.pushups"
        >
      </fieldset>

      <fieldset>
        <label for="situps">Sit-ups</label>

        <input
          type="number"
          name="situps"
          id="situps"
          step="10"
          v-model="fitness.situps"
        >
      </fieldset>

      <fieldset>
        <label for="squats">Squats</label>

        <input
          type="number"
          name="squats"
          id="squats"
          step="10"
          v-model="fitness.squats"
        >
      </fieldset>

      <fieldset>
        <label for="calfRaises">Calf Raises</label>

        <input
          type="number"
          name="calfRaises"
          id="calfRaises"
          step="10"
          v-model="fitness.calfRaises"
        >
      </fieldset>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'fitness',

    props: ['fitness']
  }
</script>

<style scoped>
  .help-text {
    text-align: center;
  }
</style>
