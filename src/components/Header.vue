<template>
  <h2>{{ text }}</h2>
</template>

<script>
export default {
  name: 'Text',
  props: {
    text: String,
  }
}
</script>