<template>
  <div>
    <h2>Event Handler Header</h2>
    Listening to events

    <button v-on:click="counter += 1;">Add 1</button>
    <p>The button above has been clicked {{ counter }} times.</p>
  </div>
</template>
<script>
export default {
  name: "EventHandler",
  data() {
    return {
      counter: 0
    };
  }
};
</script>
