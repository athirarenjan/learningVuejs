<template style="width:100%;float:left;">
  <div>
    <div v-if="hideComponent">
      <h2>Event Handler Header</h2>
      Listening to events

      <button v-on:click="incrementCounter">Add 1</button>
      <button v-on:click="warn('Form cannot be submitted yet.', $event);">
        Submit
      </button>
      <p>The button above has been clicked {{ counter }} times.</p>
      <h5>Keyboard events</h5>
      <input v-on:keyup.enter="submittingThroughKeyboard" /> <br /><br />
    </div>
    <div v-else><form-input></form-input></div>
    <div><a href="javascript:;" v-on:click="nextPage"> Next Page </a></div>
  </div>
</template>
<script>
import FormInput from "@/components/FormInput";
export default {
  name: "EventHandler",
  data() {
    return {
      counter: 0,

      hideComponent: true
    };
  },
  components: {
    FormInput
  },
  methods: {
    incrementCounter: function(Event) {
      this.counter += 1;
      this.greet(Event);
    },
    greet: function(e) {
      alert("Event" + e);
    },
    warn: function(message, event) {
      if (event) {
        event.preventDefault();
        alert(message);
      }
    },
    submittingThroughKeyboard: function() {
      alert("Submitted through key up event");
    },
    nextPage: function() {
      this.hideComponent = !this.hideComponent;
    }
  }
};
</script>
