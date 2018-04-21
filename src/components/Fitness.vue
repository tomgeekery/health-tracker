<template>
  <div>
    <h1>Fitness</h1>
    <fieldset>
      <label for="pushups">Push-ups</label>
      <input type="number" name="pushups" id="pushups" step="10" v-model="pushups">
    </fieldset>
    <fieldset>
      <label for="situps">Sit-ups</label>
      <input type="number" name="situps" id="situps" step="10" v-model="situps">
    </fieldset>
    <fieldset>
      <label for="pushups">Squats</label>
      <input type="number" name="squats" id="squats" step="10" v-model="squats">
    </fieldset>
    <fieldset>
      <label for="pushups">Calf Raises</label>
      <input type="number" name="calfRaises" id="calfRaises" step="10" v-model="calfRaises">
    </fieldset>
  </div>
</template>

<script>
  export default {
    name: 'fitness',

    data () {
      return {
        pushups: 0,
        situps: 0,
        squats: 0,
        calfRaises: 0
      }
    }
  }
</script>