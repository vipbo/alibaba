<template>
  <div id="app">
    <Parent msg="parent"/>
  </div>
</template>

<script>
import Parent from './components/Parent.vue'

export default {
  name: 'app',
  components: {
    Parent
  }
}
</script>

<style>
#app {

}
</style>
