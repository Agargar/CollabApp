<template>

  <div class="home">
    <div class="contain">
  <img src="@/assets/Wecollab.png" alt="Collab">
  <button onclick="window.location.href='http://localhost:8080/#/NewProject';" class="btn1">Create a project</button>
 
  <h2 class="imgtext">WeCollab est une communauté de créateurs qui ont collaboré sur plus de 2000 projets ! </h2>
</div>
 
    
   
<b-container>
    <h1>  </h1>
  </b-container>

<b-container>
    <h2> Ongoing Projects </h2>
  </b-container>
    <project-list></project-list>

    <b-container>
<h1>


</h1>


<br>
<br>
<br>
<br><br>
<br><br>
  </b-container>
  

    
   

  </div>
</template>

<script>
// @ is an alias to /src
import ProjectLists from '@/components/ProjectLists.vue';


import  '@/assets/Wecollab.png';
    


export default {
  name: 'HomeView',
  components: {
       "project-list" : ProjectLists
    
       
      

  }
  
}
</script>

<style>
.bv-example-row{
  width: 100%;
}
* {
 
 font-family: 'Poppins', sans-serif;
}
h2{
  padding-top: 50px;
  padding-bottom: 10px;
  padding-left: 0px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
/* Container needed to position the button. Adjust the width as needed */
.container {
  position: relative;
  width: 50%;
}

/* Make the image responsive */
.contain img {
  width: 100%;
  height: auto;
  margin-top: 0px;
}

/* Style the button and place it in the middle of the container/image */
.contain .btn1 {
  position: absolute;
  top: 55%;
  left: 25%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  background-color: rgb(13, 12, 12);
  color: rgb(255, 255, 255);
  font-size: 16px;
  padding: 12px 24px;
  border: none;
  cursor: pointer;
  border-radius: 0px;
}
.imgtext{
  position: absolute;
  top: 40%;
  left: 40%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  color: rgb(0, 0, 0);
  font-size: 30px;
  padding: 12px 24px;
  font-weight: 600;
  border: none;
  cursor: pointer;
  border-radius: 0px;
}

.contain .btn1:hover {
  background-color: black;
}



</style>
