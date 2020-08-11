<template>
  <div>
    <h3>{{ postTitle }}</h3>
    {{ likes }}
    {{ msg }}
    <!-- {{ post.title }}
    -->
    <!-- <ul>
      <li v-for="post in posts" v-bind:key="post.id">{{ post.title }}</li>
    </ul>-->

    <TestChild v-bind:posts="posts"></TestChild>
    {{ object.name + " " + object.id + " " + object.age }}
    {{ person }}
  </div>
</template>
<script>
import TestChild from "./TestChild"

export default {
  name: "Test",
  components: {
       TestChild
  },
  props: {
    posts: Array,
    postTitle: String,
    likes: {
         type: Number,
         default: 100
    },
    object: {
        type: Object,
        default: 
              () => {
                   // Statements
                   // K co return
                   return {
                        name:"Vang",
                         age:18,
                         id:"ITITIU17063"
                    }   
             },
        },
    person: Function
  },
  data: function() {
    return {
      msg: "This is message"
      //   posts:[
      //        {name:"name 1", author:"Thuan"},
      //        {name:"name 2", author:"Thuan Tran"},
      //        {name:"name 3", author:"Thuan Tran Dinh"},
      //   ]
    };
  }
};
//   {
//
//     posts: [
//       { title: "this is title 1" },
//       { title: "this is title 2" },
//       { title: "this is title 3" }
//     ]
//   }
</script>
<style scoped>
</style>