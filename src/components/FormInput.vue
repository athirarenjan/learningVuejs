<template>
  <div>
    <form>
      <h5>Form Inputs</h5>
      <input v-model="message" placeholder="edit me" />
      <p>Message is: {{ message }}</p>
      <span>Multiline message is:</span>
      <p style="white-space: pre-line;">{{ message2 }}</p>
      <br />
      <textarea v-model="message2" placeholder="add multiple lines"></textarea>
      <br /><br />
      <input type="checkbox" id="checkbox" v-model="checked" />
      <label for="checkbox">{{ checked }}</label>
      <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
      <label for="jack">Jack</label>
      <input type="checkbox" id="john" value="John" v-model="checkedNames" />
      <label for="john">John</label>
      <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
      <label for="mike">Mike</label> <br />
      <span>Checked names: {{ checkedNames }}</span> <br /><br />
      <select v-model="selected">
        <option disabled value="">Please select one</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>
      </select>
    </form>
  </div>
</template>

<script>
export default {
  name: "FormInput",
  data() {
    return {
      message: "",
      message2: "",
      checked: false,
      checkedNames: [],
      selected: ""
    };
  }
};
</script>
