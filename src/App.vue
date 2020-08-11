<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <Test
      v-bind:likes="likes"
      v-bind:posts="posts"
      v-bind:person="person('thuan', 'tran')"
      msg="thuan"
      postTitle="This is post Title"
    ></Test>
    <div id="app">
      {{ info }}
    </div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Test from "./components/Test";


export default {
  name: "App",
  components: {
    // HelloWorld,
    Test,
  },
  data: function() {
    return {
      likes: 45,
      posts: [
        { id: 1, title: "My journey with Vue" },
        { id: 2, title: "Blogging with Vue" },
        { id: 3, title: "Why Vue is so fun" },
      ],
      Objects: {
        name: "Thuan",
        age: 18,
        id: "ititiu17112",
      },
      person: function(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
        alert(firstName + lastName);
        alert(this.Objects.name);
        alert(this.Objects.age + this.Objects.name + this.Objects.id);
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
