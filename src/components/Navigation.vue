<template>
  <header>
    <h1 class="header-heading">
      <a 
        href="#"
        @click.prevent="changePage('summary')"
      >100 Days of Health</a>
    </h1>

    <div class="options">
      <button
        class="option icon-bicycle"
        @click="changePage('fitness')"
      ></button>

      <button
        class="option icon-food"
        @click="changePage('food')"
      ></button>
    </div>
  </header>
</template>

<script>
  export default {
    name: 'navigation',
    props: ['page'],
    methods: {
      changePage (page) {
        this.$emit('change-page', page)
      }
    }
  }
</script>

<style scoped>
  .header-heading {
    background-color: #4ea5d9;
    color: #fff;
    margin: 0;
    padding: 2rem;
    text-align: center;
  }

  .options {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .option {
    background-color: #083d77;
    padding: 1rem;
    text-align: center;
    width: 50%;
  }

  .option:first-child {
    border-right: 1px solid;
  }

  .option::before {
    color: #fff;
    font-size: 3rem;
  }
</style>
