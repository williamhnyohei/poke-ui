<template>
  <button class="pokeball-button">
    <div class="pokeball-top"></div>
    <div class="pokeball-bottom"></div>
    <div class="pokeball-middle"></div>
    <span class="pokeball-center"></span>
  </button>
</template>

<script>
export default {
  name: 'PokemonButton',
  props: {
    placeholder: String
  },
  methods: {
    onClick() {
      this.$emit('click');
    }
  }
};
</script>

<style scoped>
.pokeball-button {
  position: relative;
  width: 120px;
  height: 60px;
  background-color: #ff3f3f;
  border-radius: 15px 50px 50px 15px;
  border: solid 2px black;
  box-sizing: border-box;
  overflow: hidden;
}

.pokeball-top, .pokeball-bottom {
  position: absolute;
  top: 0;
  width: 100%;
  height: 30px;
  background-color: #fff;
  border-radius: 15px 50px 0 0;
}

.pokeball-top {
  box-shadow: 0 -1px 0 black;
}

.pokeball-bottom {
  top: 30px;
  box-shadow: 0 1px 0 black;
}

.pokeball-middle {
  position: absolute;
  top: 15px;
  left: 15px;
  width: 90px;
  height: 30px;
  background-color: #000;
  border-radius: 0 50px 50px 0;
  box-shadow: inset -2px -2px 0 rgba(255, 255, 255, 0.2);
}

.pokeball-center {
  display: block;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 50px;
  height: 50px;
  background-color: #fff;
  border-radius: 50%;
  border: solid 2px black;
}

.pokeball-center:before, .pokeball-center:after {
  content: "";
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 30px;
  height: 2px;
  background-color: #000;
}

.pokeball-center:before {
  transform: translate(-50%, -50%) rotate(45deg);
}

.pokeball-center:after {
  transform: translate(-50%, -50%) rotate(-45deg);
}


</style>
