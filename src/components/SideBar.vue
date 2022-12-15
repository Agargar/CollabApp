<template>
    <div class="container">
      <!--left-->
      <div class="left-sidebar">
        <div class="imp-links">
          <router-link to="/"
            ><img src="../assets/images/upload.png" />Create a new
            post</router-link
          >
          <router-link to="/"
            ><img src="../assets/images/group.png" />Your colabs</router-link
          >

          <router-link to="/"
            ><img src="../assets/images/follow.png" />Join a
            community</router-link
          >

          <router-link to="/"
            ><img src="../assets/images/friends.png" />Friends
          </router-link>
        </div>
        <div class="recent">
          <p>Recently opened</p>
          <router-link to="/"
            ><img src="../assets/images/recent-1.png" />Writing a
            story</router-link
          >
          <router-link to="/"
            ><img src="../assets/images/recent-2.png" />Tetris
            heuristics</router-link
          >
        </div>
      </div>
      </div>
</template>

<script>
export default {
  
  
};

</script>

<style>
.left-sidebar {
  flex-basis: 25%;
  position: sticky;
  top: 70%;
  align-self: flex-start;
}
</style>