<template>
  <header>
    <h1 class="header-heading">100 Days of Health</h1>
    <div class="options">
      <button class="option icon-bicycle"></button>
      <button class="option icon-food"></button>
    </div>
  </header>
</template>

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