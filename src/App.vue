
<template>
  <div id="app">
    <Navbar />
    <b-container class="m-5">
      <Datos />
    </b-container>
  </div>
</template>

<script>
import Navbar from "./NavBar.vue";
import AllFriends from "./AllFriends";
import OnlineFriends from "./AllOnlineFriends";
import Blogs from "./Blogs";
import Datos from "./datos.vue";

export default {
  name: "app",
  components: {
    Navbar,
    AllFriends,
    OnlineFriends,
    AllFriends,
    Blogs,
    Datos,
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
