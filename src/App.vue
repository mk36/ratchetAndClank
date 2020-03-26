<style lang="scss">

</style>

<template>
  <div id="app">
   <test-comp></test-comp>
    <p>test</p>
      <div class="home">
          <p>hello</p>
          <div class="columns">
              <div class="column">1</div>
              <div class="column">2</div>
              <div class="column">3</div>
              <div class="column">4</div>
              <div class="column">5</div>
          </div>
      </div>
  </div>
</template>

<script>
import "./styles/styles.scss";
import TestComp from './components/test-comp/test-comp.vue';

export default {
  name: 'App',
  components: {
    TestComp
  }
}
</script>
