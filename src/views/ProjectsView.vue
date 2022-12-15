<template>
    <div class="Projects">
   

      <b-container class="bv-example-row">

   <h2>Catégories Populaires</h2>     
  <b-row>
    <b-col> <b-card onclick="window.location.href='http://localhost:8080/#/Projects';"
    overlay
    img-src="https://i.postimg.cc/G3BsRT8h/tech.png"
    img-alt="Card Image"
    text-variant="white"
    title="Développement"
  
  >
    
  </b-card>
 </b-col>
    <b-col> <b-card onclick="window.location.href='http://localhost:8080/#/Projects';"
    overlay
    img-src="https://i.postimg.cc/RZKdGbQf/photography.png"
    img-alt="Card Image"
    text-variant="white"
    title="Cinéma et Photographie"
   
  >
   
  </b-card>
</b-col>
    <b-col> <b-card onclick="window.location.href='http://localhost:8080/#/Projects';"
    overlay
    img-src="https://i.postimg.cc/YS1bby7Z/mic.png"
    img-alt="Card Image"
    text-variant="white"
    title="Musique"
   
  >
    
  </b-card>
</b-col>
 <b-col> <b-card onclick="window.location.href='http://localhost:8080/#/Projects';"
    overlay
    img-src="https://i.postimg.cc/26CfCKxN/novel.png"
    img-alt="Card Image"
    text-variant="white"
    title="Histoire"
   
  >
    
  </b-card>
</b-col>
  </b-row>

  <h2>Liste Des Projets</h2>  
  <div class="visible">
  <project-list> </project-list>
  </div>

</b-container>

    </div>
   
     
    
    
  </template>
  

<script>
import ProjectLists from '@/components/ProjectLists.vue';
export default{
  components : {
  "project-list" : ProjectLists
  }
}


</script>


<style>


</style>