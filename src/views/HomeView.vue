<template>
  <div class="home">
    <h2>Home</h2>
    <p>Name: {{ name }} and Age: {{ age }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  setup() {
    let name = "Lisa";
    let age = 30;

    const handleClick = () => {
      console.log("you clicked me");
    };

    return { name, age, handleClick };
  },
  created() {
    console.log("created");
  },
  mounted() {
    console.log("mounted");
  },
};
</script>

<style></style>
