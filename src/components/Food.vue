<template>
  <div>
    <fieldset>
      <label for="foodEntry">Food Log</label>
      <textarea rows="10" name="foodEntry" id="foodEntry" v-model="food.log"></textarea>
    </fieldset>
    <fieldset>
      <button @click="storeFoodLog">Save</button>
    </fieldset>
  </div>
</template>

<script>
  export default {
    name: 'food',

    props: ['food'],

    methods: {
      storeFoodLog () {
        // Save the food log in local storage.
        localStorage.healthTrackerFoodLog = this.food.log
      }
    }
  }
</script>

