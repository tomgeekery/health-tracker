<template>
  <div>
    <p class="help-text">Keep track of what you eat today here!</p>
    <fieldset>
      <label for="foodEntry">Food Log</label>
      <textarea rows="10" name="foodEntry" id="foodEntry" v-model="food.log"></textarea>
    </fieldset>
  </div>
</template>

<script>
  export default {
    name: 'food',
    props: ['food']
  }
</script>

<style scoped>
  .help-text {
    text-align: center;
  }
</style>
