<template>
  <div>
    <ul>
      <li v-for="post in posts" v-bind:key="post.id">{{ post.title }}</li>
    </ul>
  </div>
</template>
<script>
export default {
     name:"TestChild",
     props:{
          posts:Array
     }
};
</script>
<style scoped>
</style>