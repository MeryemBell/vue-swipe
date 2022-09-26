<template>
  <div id="app">
    <SwipeBox ref="myswipe" @onChange="mySwipeChanged" speed="150">
      <button @click="next">prvs</button>
      <div style="width: 400px; height: 200px; border: 1px solid black">
        <div v-for="image in images" :key="image.id">
          <img src="" /><button @click="previous">></button>
        </div>
      </div>
    </SwipeBox>
    <button @click="next">next</button>
  </div>
</template>

<script>
import SwipeBox from '@shopid/vue3-swipe-box';

export default {
  name: 'HelloWorld',
  components: {
    SwipeBox,
  },
};
</script>
