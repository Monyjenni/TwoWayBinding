<template>
  <div id="app">
    <h1 class="h1">Course Tutorial</h1>
    {{ greeting }}
    <input v-model="greeting" />
    <hr />
    <!-- v-if is used when we set true to that var in script is true -->
    <!-- v-show is the same as v-if on DOM but there is still on there ,the diff is display: none-->

    <!-- ------------------------------------------------------------------------------------------------------------- -->
    <!-- even&method -->
    <!-- @ is same as v-on: -->
    <button @click="isVisible = !isVisible">Toggle Box</button>
    <div v-if="isVisible" class="box"></div>
    <!-- <div v-else-if="isVisible1" class="box-two"></div>
    <div v-else class="box-three"></div> -->
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      data: 0,
      greeting: "Hey Friend!",
      isVisible: false,
      // isVisible1: false,
    };
  },
};
</script>

<style>
.h1 {
  font-size: 50px;
  font-weight: 50px;
}
.box {
  background-color: pink;
  height: 200px;
  width: 200px;
}
.box-two {
  background-color: aqua;
  height: 200px;
  width: 200px;
}
.box-three {
  background-color: black;
  height: 200px;
  width: 200px;
}
</style>
