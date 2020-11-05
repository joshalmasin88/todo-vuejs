<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-md-6 mx-auto">
          <h1 class="text-center my-3">Todo List:</h1>
          <Card />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from './componets/Cards'

export default {
  name: 'app',
  components: {
    Card
  },
  data () {
    return {
      
    }
  }
}
</script>

<style>

</style>
