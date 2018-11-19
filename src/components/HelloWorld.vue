<template v-if="show">
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Learning Links</h2>
    <ul>
      <li>
        <a href="javascript:;" target="_blank" v-on:click="toggle">
          Event Handling
        </a>
      </li>
    </ul>
  </div>
</template>
<template v-else> 
<event-handler>
</event-handler>
</template>

<script>
import EventHandler from "@/components/EventHandler"
export default {
  name: "HelloWorld",
  components:{EventHandler},
  data() {
    return {
      msg: "Learning Vue.js",
      show: true
    };
  },
  methods: {
    toggle: function() {
      this.show = !this.show;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
