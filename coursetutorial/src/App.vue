<template>
  <div id="app">
    <h1 class="h1">Course Tutorial</h1>
    {{ greeting }}
    <!-- !!! is to add in console -->
    <input @keyup.enter="greet(greeting + '!!!!!')" v-model="greeting" />
    <hr />
    <!-- v-if is used when we set true to that var in script is true -->
    <!-- v-show is the same as v-if on DOM but there is still on there ,the diff is display: none-->

    <!-- ------------------------------------------------------------------------------------------------------------- -->
    <!-- even&method -->
    <!-- @ is same as v-on: -->
    <button @click.prevent.stop="toggleBox">Toggle Box</button>
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
      greeting: "Sup Jen",
      isVisible: false,
      // isVisible1: false,
    };
  },
  // method here is a function that is associated with a class or an object, and define the behavior of the class or object.
  //toggle here is an event
  //event --> method
  methods: {
    toggleBox() {
      // this here is a constructor that initialize an object when it is created.
      this.isVisible = !this.isVisible;
    },
    greet(greeting) {
      //greeting is passed so no need to this for initialization
      console.log(greeting);
    },
  },
};
</script>

<style>
.h1 {
  font-size: 50px;
  font-weight: 50px;
}
.box {
  background-image: url("one_piece.jpg");
  height: 1000px;
  width: 1000px;
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
