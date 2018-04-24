<template>
  <div id="app">
    <Navigation
      :page="page"
      @change-page="changePage"
    ></Navigation>

    <div class="app-wrapper">
      <Summary
        :fitness="fitness"
        :food="food"
        v-if="page === 'summary'"
      ></Summary>

      <Fitness
        :fitness="fitness"
        v-if="page === 'fitness'"
      ></Fitness>

      <Food
        :food="food"
        v-if="page === 'food'"
      ></Food>
    </div>
  </div>
</template>

<script>
import Fitness from './components/Fitness'
import Food from './components/Food'
import Summary from './components/Summary'
import Navigation from './components/Navigation'

export default {
  name: 'app',

  components: {
    Fitness,
    Food,
    Navigation,
    Summary
  },

  data () {
    return {
      fitness: {
        pushups: 0,
        situps: 0,
        squats: 0,
        calfRaises: 0
      },

      food: { log: '' },
      page: 'summary'
    }
  },

  methods: {
    changePage (page) {
      this.page = page
    }
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

  a {
    color: #fff;
    text-decoration: none;
  }

  .app-wrapper {
    padding: 1rem;
  }
</style>
