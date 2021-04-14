<template>
  <Header text="Header" />
  <Count />
</template>

<script>
import Count from './components/Count.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header,
    Count,
  }
}
</script>
