<template>
    <div>
        <b-navbar toggleable="lg" type="dark" class="nav-background">
          <b-navbar-brand href="#">
      <img src="@/assets/logoAppW.png" alt="logo">
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item to="/">Home</b-nav-item>
        <b-nav-item to="/Projects">Projects</b-nav-item>
        <b-nav-item to="/Profile">Profile</b-nav-item>
        <b-nav-item to="/about">About</b-nav-item>

       
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-form>
       
          <b-button onclick="window.location.href='http://localhost:8080/#/LoginView';" variant="light">Se connecter</b-button>
        </b-nav-form>

       
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
    </div>

</template>

<script>


</script>
  export default{

  }
  <style >
  .nav-background{
    background-color: #171717;
    height : 100px;
  }
 .btn2 {
 
  background-color: rgb(209, 209, 209);
  color: rgb(30, 30, 30);
  font-size: 16px;
  padding: 12px 24px;
  border: none;
  cursor: pointer;
  border-radius: 0px;
  }
 
</style>