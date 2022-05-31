<script>
import MyButton from "./MyButton.vue";
import MyInput from "./MyInput.vue";

export default {
  components: {
    MyButton,
    MyInput,
  },

  data() {
    return {
      username: {
        value: "",
      },
    };
  },

  methods: {
    update(payload) {
      this[payload.name] = {
        value: payload.value,
      };
    },
    submit() {
      console.log("Submit", this.username.value);
    },
  },
};
</script>

<template>
  <main>
    <my-input name="Username" @update="update" :value="username.value" />
    <my-button
      background="darkSlateblue"
      color="white"
      value="Submit"
      @clicked="submit"
    />
  </main>
</template>
