<template>
  <div>
    <p>Here's a summary of what you've done so far today!</p>

    <div>Pushups: {{ fitness.pushups }}</div>
    <div>Situps: {{ fitness.situps }}</div>
    <div>Squats: {{ fitness.squats }}</div>
    <div>Calf Raises: {{ fitness.calfRaises }}</div>

    <div>Food Log</div>
    <div>{{ food.log }}</div>
  </div>
</template>

<script>
  export default {
    name: 'summary',
    props: [
      'food',
      'fitness'
    ]
  }
</script>
