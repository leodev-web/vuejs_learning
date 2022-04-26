<script>
import MyButton from "./MyButton.vue";
import MyInput from "./MyInput.vue";

export default {
  components: {
    MyButton,
    MyInput,
  },
};
</script>

<template>
  <main>
    <my-input name="Username" />
    <my-button background="darkSlateblue" color="white" value="Submit" />
  </main>
</template>
