<template>
  <div class="container">
    <buttonPoke
      placeholder="capture"
      @click="handleClick"
    />
  </div>
</template>

<script>
import buttonPoke from './components/button.vue';

export default {
  name: 'App',
  components: {
    buttonPoke,
  },
  methods: {
    handleClick() {
      console.log('capturado HAHAHAHA')
    }
  },
}
</script>

<style scoped>
.container {
  width: 500px;
  height: 500px;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100vw;
  height: 100vh;
  background-color: #2c3e50;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
