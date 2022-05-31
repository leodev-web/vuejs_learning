<template>
  <div class="label">
    <label v-bind:for="name">Username:</label>
    <input v-bind:id="name" :value="value" @input="input" />
  </div>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    value: {
      type: String,
      required: true,
    },
  },

  methods: {
    input($event) {
      this.$emit("update", {
        name: this.name.toLowerCase(),
        value: $event.target.value,
      });
    },
  },
};
</script>

<style scoped>
.input {
  display: flex;
  flex-direction: column;
}
.label {
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  margin-bottom: 5px;
}
.error {
  color: red;
}
.input {
  width: 100%;
}
input {
  box-sizing: border-box;
  padding: 10px;
  border-radius: 8px;
  border: 1px solid silver;
  margin: 2px;
  font-size: 16px;
  width: 100%;
  cursor: pointer;
}
</style>