<template>
  <div id="HelloWorld">
    <SwipeBox ref="myswipe" @onChange="mySwipeChanged" speed="150">
      <button @click="next">prvs</button>
      <div style="width: 400px; height: 200px; border: 1px solid black">
        <div v-for="image in images" :key="image.id">
          <img src="#" /><button @click="previous">></button>
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
  data: () => {
    return {
      index: 0,
    };
  },

  methods: {
    next: function (x) {
      this.$refs.myswipe.swipetoNext();
    },
    previous: function (x) {
      this.$refs.myswipe.swipetoPrevious();
    },
  },
};
</script>

<style>
#HelloWorld {
  display: flex;
  flex-direction: column;
  align-items: center;
}
button {
  margin: 0.5rem;
  padding: 0.5rem;
}
</style>
