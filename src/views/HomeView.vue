<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{ userOne.name }} - {{ userOne.age }} - {{ nameOne }}</p>
    <button @click="updateUserOne">Update User</button>
    <h2>Reactive</h2>
    <p>{{ userTwo.name }} - {{ userTwo.age }} - {{ nameTwo }}</p>
    <button @click="updateUserTwo">Update User</button>
  </div>
</template>

<script>
import { ref, reactive } from "vue";

export default {
  name: "HomeView",
  setup() {
    const userOne = ref({ name: "lisa", age: 30 });
    const userTwo = reactive({ name: "marie", age: 35 });

    const nameOne = ref("lisa");
    const nameTwo = reactive("marie");

    const updateUserOne = () => {
      userOne.value.age = 35;
    };

    const updateUserTwo = () => {
      userTwo.age = 36;
    };

    return { userOne, updateUserOne, userTwo, updateUserTwo, nameOne, nameTwo };
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
