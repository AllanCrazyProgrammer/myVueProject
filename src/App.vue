
<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar />
    <AllFriends :friends="friends" @delete="deleteFriend" />
    <OnlineFriends :friends="friends" />
    <Blogs />
  </div>
</template>

<script>
import Navbar from "./NavBar.vue";
import AllFriends from "./AllFriends";
import OnlineFriends from "./AllOnlineFriends";
import Blogs from "./Blogs";

export default {
  name: "app",
  components: {
    Navbar,
    AllFriends,
    OnlineFriends,
    AllFriends,
    Blogs,
  },
  data() {
    return {
      title: "Bienvenido al 2021, Allan",
      friends: [
        { name: "Allan", online: true },
        { name: "Toad", online: false },
        { name: "Bryan", online: true },
        { name: "Jason", online: false },
      ],
    };
  },
  methods: {
    deleteFriend(payload) {
      console.log(payload);
      this.friends = this.friends.filter((friend) => {
        return friend.name !== payload;
      });
    },
  },
};
</script>

<style>
h1 {
  color: blueviolet;
  text-align: center;
  font-weight: normal;
}
</style>
