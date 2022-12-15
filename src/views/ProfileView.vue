<template>
  <div class="Collabs">

    <div class="row">
        <div class="col-md-3 border-right">
            <div class="d-flex flex-column align-items-center text-center p-3 py-5"><b-avatar id="avatar" src="https://placekitten.com/300/300" size="8rem"></b-avatar><span class="font-weight-bold">@Miaou</span> <span class="text-black-50">Membre depuis 2019</span><b-badge class="badge-b" pill variant="primary">developer</b-badge><span> </span></div>
        </div>
        <div class="col-md-9 border-right">
            <div class="p-3 py-5">
                <div class="d-flex justify-content-between align-items-center mb-3">
                    <h4 class="text-right">Paramètres de profil </h4>
                </div>
                <div>
  <b-tabs content-class="mt-3">
    <b-tab title="Profile" active>
      <p>Prénom :            XXXXX</p>
      <p>Nom :               YYYYY</p>
      <p>Date de Naissance : XX/YY/ZZ</p>
      <p>e-mail :            sdsdsYYYYY@gmail.com</p>
      <p>Membre depuis :     12/yy/zz</p>
      
    </b-tab>
    <b-tab title="Projets"><p>
      <b-list-group>
  <b-list-group-item onclick="window.location.href='http://localhost:8080/#/ProjectsoView';" class="d-flex justify-content-between align-items-center">
    Design d'une map 3D
    <b-badge variant="primary" pill>achevé</b-badge>
  </b-list-group-item>

  <b-list-group-item onclick="window.location.href='http://localhost:8080/#/ProjectsoView';" class="d-flex justify-content-between align-items-center">
    Créer une charte graphique pour un site e-commerce
    <b-badge variant="primary" pill>Invitation en cours</b-badge>
  </b-list-group-item>

  <b-list-group-item onclick="window.location.href='http://localhost:8080/#/ProjectsoView';" class="d-flex justify-content-between align-items-center">
    Musique pour bande Annonce
    <b-badge variant="primary" pill>En cours</b-badge>
  </b-list-group-item>
</b-list-group>

    </p></b-tab>
    <b-tab title="Favoris"><p>Aucun favoris pour l'instant!</p></b-tab>
    <b-tab title="Messages"><p>Vous n'avez reçu aucun message!</p>
    
    </b-tab>
  </b-tabs>
</div>
                
            </div>
        </div>
        
    </div>
</div>



  </template>


<style>
  @import url(http://fonts.googleapis.com/css?family=Calibri:400,300,700);
*{
  font-family: Verdana, Geneva, Tahoma, sans-serif;


}


.font-weight-bold {
  padding-top: 10px;
}

.text-black-50{
  padding-top: 10px;
}

.badge-b{
  margin-top: 10px;
}
.labels {
    font-size: 11px
}
p{

  position: relative;
  text-align: left;
  font-weight: 500;
  font-size: medium;

}

h4{
  font-weight: 600;


}
</style>
