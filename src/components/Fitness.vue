<template>
  <div>
    <div class="wrapper">
      <div class="form-fields">
        <fieldset class="form-wrapper">
          <label for="pushups">Push-ups</label>

          <input
            type="number"
            name="pushups"
            id="pushups"
            class="number-field"
            step="10"
            min="0"
            v-model="fitness.pushups"
          >
        </fieldset>

        <fieldset class="form-wrapper">
          <label for="situps">Sit-ups</label>

          <input
            type="number"
            name="situps"
            id="situps"
            class="number-field"
            step="10"
            v-model="fitness.situps"
          >
        </fieldset>

        <fieldset class="form-wrapper">
          <label for="squats">Squats</label>

          <input
            type="number"
            name="squats"
            id="squats"
            class="number-field"
            step="10"
            v-model="fitness.squats"
          >
        </fieldset>

        <fieldset class="form-wrapper">
          <label for="calfRaises">Calf Raises</label>

          <input
            type="number"
            name="calfRaises"
            id="calfRaises"
            class="number-field"
            step="10"
            v-model="fitness.calfRaises"
          >
        </fieldset>
      </div>
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

  .form-fields {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .form-wrapper {
    text-align: center;
    width: 45%;
  }

  .number-field {
    text-align: center;
    width: 10rem;
  }
</style>
