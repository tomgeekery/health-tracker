<template>
  <div id="app">
    <Header></Header>
    <div class="app-wrapper">
      <Fitness></Fitness>
      <Food></Food>
    </div>
  </div>
</template>

<script>
import Fitness from './components/Fitness'
import Food from './components/Food'
import Header from './components/Header'

export default {
  name: 'app',
  components: {
    Fitness,
    Food,
    Header
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
  }

  html {
    font-size: 2vw;
  }

  body {
    color: #122c34;
    font-family: 'Lato', sans-serif;
    font-size: 2rem;
    margin: 0;
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
    color: #6d6d6d;
    padding: 0.5rem;
    width: 100%;
  }

  ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }

  button {
    border: 0;
    cursor: pointer;
  }

  .heading {
    background-color: #208aae;
    color: #fff;
    padding-bottom: 1rem;
    padding-top: 1rem;
    text-align: center;
  }

  .wrapper {
    padding: 1rem;
  }
</style>
