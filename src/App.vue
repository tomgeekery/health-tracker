<template>
  <div id="app">
    <Fitness></Fitness>
    <Food></Food>
  </div>
</template>

<script>
import Fitness from './components/Fitness'
import Food from './components/Food'

export default {
  name: 'app',
  components: {
    Fitness,
    Food
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
  }

  body {
    color: #6d6d6d;
  }

  fieldset {
    border: 0;
    padding: 0.5rem 0;
  }

  label {
    display: block;
    margin-bottom: 0.25rem;
  }

  input,
  textarea {
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 0.25rem;
    padding: 0.5rem;
    width: 100%;
  }
</style>
