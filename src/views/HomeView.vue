<template>
  <div class="home">
    <h2>Home</h2>
    <p class="user-info">Name: {{ name }}, Age: {{ age }}</p>
    <input type="text" v-model="name" />
    <button @click="handleClick">Update User</button>
    <button @click="age++">Increase Age</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "HomeView",
  setup() {
    const name = ref("Lisa");
    const age = ref(30);

    const handleClick = () => {
      name.value = "Marie";
      age.value = 35;
    };

    return { name, age, handleClick };
  },
  data() {
    return {
      score: 5,
    };
  },
};
</script>

<style>
.user-info {
  color: blueviolet;
}
button {
  background: blueviolet;
  color: #fff;
  padding: 5px;
  margin: 5px;
  border: #fff;
  border-radius: 5px;
}
</style>
