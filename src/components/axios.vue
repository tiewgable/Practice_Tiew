<template>
  <div>
    <p v-for="manu in manu" :key="manu.id">{{ manu.id }}-{{ manu.Title }}</p>
    <input placeholder="id" v-model="id" />
    <input placeholder="Title" v-model="Title" />
    <button @click="post()">post</button>
    <button @click="put()">Put</button>
    <button @click="remove()">Delete</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      text: "test",
      manufacturer: [{ id: 1, Title: "test" }],
    };
  },
  created() {
    this.get();
  },
  methods: {
    get() {
      axios.get("").then((respone).then((respone => {this.manufacturer = respone.data)
      
    },
  },
};
</script>