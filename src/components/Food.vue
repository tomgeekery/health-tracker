<template>
  <div>
    <h1>Food</h1>
    <fieldset>
      <label for="pushups">Food Entry</label>
      <textarea rows="10" name="foodEntry" id="foodEntry" v-model="foodEntry"></textarea>
    </fieldset>
  </div>
</template>

<script>
  export default {
    name: 'food',

    data () {
      return {
        foodEntry: ''
      }
    }
  }
</script>