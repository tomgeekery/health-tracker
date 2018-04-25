<template>
  <fieldset>
    <label for="foodEntry">Food Log</label>
    <textarea rows="10" name="foodEntry" id="foodEntry" v-model="food.log"></textarea>
  </fieldset>
</template>

<script>
  export default {
    name: 'food',
    props: ['food']
  }
</script>

