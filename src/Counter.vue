<template>
    <div class="counter">
        {{ count }}
        <div class="counter__button" @click="increment">+</div>
    </div>
</template>


<script>
import store from "./store/NotificationStore";

export default {
  data() {
    return {
      state: store.state
    };
  },
  methods: {
    increment() {
      store.increment();
    }
  },
  computed: {
    count: function() {
      return this.state.count;
    }
  }
};
</script>

<style>
.counter {
  font-weight: bold;
}

.counter__button {
  margin: auto;
  padding: 5px 5px;
  width: 30px;
  border: solid black 1px;
}
</style>
