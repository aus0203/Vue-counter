<template>
  <h1>{{ title }}</h1>
  <div class="counter">
    <CounutingButton symbol="-" @click="decrement"/>
    <h3 class="value">{{ value }}</h3>
    <CounutingButton symbol="+" @click="increment"/>
  </div>
</template>

<script>
import CounutingButton from "./components/y-button.vue";

export default {
  name: "App",
  components: { CounutingButton },
  data() {
    return {
      title: "Vue Counter practice",
      value: 0,
    };
  },
  methods:{
    decrement(){
      this.value--;
    },
    increment(){
      this.value++;
    }
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #f9f9f9;
}

#app {
  font-family: "Nunito Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 64px;
}

.counter {
  display: flex;
  gap: 52px;
  margin: 80px;
  justify-content: center;
  align-items: center;
}

.value{
    transition: .3s ease-in-out;
}
</style>
