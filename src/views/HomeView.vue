<template>
  <div class="home">
    <h2>Home</h2>
    <p ref="p">Name: {{ name }} and Age: {{ age }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "HomeView",
  setup() {
    const p = ref(null);

    let name = "Lisa";
    let age = 30;

    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add("msg");
      p.value.textContent = "hello islanders";
    };

    return { name, age, handleClick, p };
  },
  created() {
    console.log("created");
  },
  mounted() {
    console.log("mounted");
  },
};
</script>

<style>
.msg {
  color: aqua;
}
</style>
