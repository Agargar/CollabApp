<template>
<div class="home">
  
<div class="container mt-5"> 
  <h2>Création d'un site en Vuejs</h2>
    <div class="d-flex justify-contente-left row"> 
        <div class="col-md-10"> <div class="list"> 
            <div class="items p-2 bg-white px-3 border mt-2"> 
                <div class="d-flex justify-content-between align-items-center user-info"> 
                    <div class="d-flex flex-row align-items-center">
                        <img src="https://i.imgur.com/SzqskfC.png" width="60"> 
                        <div class="d-flex flex-column user-name-followers">
                            <span class="font-weight-bold">Bert21@</span>
                            <span id="collabn">9 Collaborations</span>
                            </div> <div></div> </div> <div><i class="fa fa-bookmark-o fa-2x text-info"></i></div> </div> <hr> <div> 
                              <p class="about"> Bonjour, je suis étudiant en Ui design et je cherche des collaborateurs pour créer un site d'aide en particuliers</p> <div class="d-flex flex-row mb-3"> <p>Besoin de :</p><span class="px-2 bg-primary text-white mr-1 rounded tags" style="height:25px">Dév front-end</span><span class="px-2 bg-success text-white mr-1 rounded tags" style="height:25px">back-end Dev</span><span class="px-2 bg-warning text-white mr-1 rounded tags" style="height:25px">Ux Designer</span></div> </div> </div>
                              <div class="container d-flex justify-content-center mt-100 mb-100" style="padding-left: 0px; padding-right: 0px">
  <div class="row">
      <div class="col-md-12">

        <div class="card">
                            <div class="card-body">
                                <h4 class="card-title">Messages</h4>
                                <h6 class="card-subtitle">Derniers messages</h6> </div>

                            <div class="comment-widgets m-b-20">

                                <div class="d-flex flex-row comment-row">
                                    <div class="p-2"><span class="round"><img src="https://i.imgur.com/uIgDDDd.jpg" alt="user" width="50"></span></div>
                                    <div class="comment-text w-100">
                                        <h5 >@Gogzila </h5>
                                        <span  id= "tal" class="px-2 bg-primary text-white mr-1 rounded tags" style="height:25px">Dév front-end</span>
                                        <div class="comment-footer">
                                            
                                        </div>
                                        <p class="m-b-5 m-t-10">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.</p>
                                    </div>
                                </div>

                                <div class="d-flex flex-row comment-row ">
                                    <div class="p-2"><span class="round"><img src="https://i.imgur.com/tT8rjKC.jpg" alt="user" width="50"></span></div>
                                    <div class="comment-text active w-100">
                                        <h5>@SonAF12</h5>
                                        <span  id= "tal" class="px-2 bg-primary text-white mr-1 rounded tags" style="height:25px">Dév front-end</span>
                                        <div class="comment-footer">
                                           
                                        </div>
                                        <p class="m-b-5 m-t-10">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.</p>
                                    </div>
                                </div>

                                <div class="d-flex flex-row comment-row">
                                    <div class="p-2"><span class="round"><img src="https://i.imgur.com/cAdLHeY.jpg" alt="user" width="50"></span></div>
                                    <div class="comment-text w-100">
                                        <h5>@shh121.</h5>
                                        <span  id= "tal" class="px-2 bg-success text-white mr-1 rounded tags" style="height:25px">back-end Dev</span>
                                        <div class="comment-footer">
                                           
                                        </div>
                                        <p class="m-b-5 m-t-10">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.</p>
                                    </div>
                                </div>

                                <div class="bg-light p-2">
                                    <div>
                          <b-form-select v-model="selected" :options="options" style="margin-bottom: 10px;" ></b-form-select>
                   
                      </div>
                    <div class="d-flex flex-row align-items-start"><img class="rounded-circle" src="https://placekitten.com/300/300" width="40"><textarea class="form-control ml-1 shadow-none textarea"></textarea></div>
                    <div class="mt-2 text-right"><button  class="btn btn-primary btn-sm shadow-none" type="button">Envoyer l'invitation</button><button class="btn btn-outline-primary btn-sm ml-1 shadow-none" type="button">Abandoner</button></div>
                </div>

                               
                               
                            </div>
                        </div>

                        

      </div>
      
  </div>
</div>
                            </div> </div>
                          
                          
                          
                          </div> </div>
                          </div>


                          
</template>
<script>
export default {
    data() {
      return {
        selected: null,
        options: [
          { value: null, text: 'Developpeur Front end' },
          { value: 'a', text: 'Designer Ui' },
          { value: 'b', text: 'Designer Ux', disabled: true },
          
        ]
      }
    }
  }
</script>

<style>
.px-2 {
  margin-left: 10px;
}
@import url(http://fonts.googleapis.com/css?family=Calibri:400,300,700);

body {
    background-color: #D32F2F;
    font-family: 'Calibri', sans-serif !important;
}
b-form-select{
    margin-bottom: 10px;
}

.card-no-border .card {
    border: 0px;
    border-radius: 4px;
    -webkit-box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.05);
    box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.05)
}

.card-body {
    -ms-flex: 1 1 auto;
    flex: 1 1 auto;
    padding: 1.25rem
}

.comment-widgets .comment-row:hover {
    background: rgba(0, 0, 0, 0.02);
    cursor: pointer;
}

.comment-widgets .comment-row {
    border-bottom: 1px solid rgba(120, 130, 140, 0.13);
    padding: 15px;
}
.comment-text:hover{
    visibility: hidden;
}
.comment-text:hover{
    visibility: visible;
}
.h2{
  margin-top: 30px;
  position: relative;
  text-align: left;
}
.label {
    padding: 3px 10px;
    line-height: 13px;
    color: #ffffff;
    font-weight: 400;
    border-radius: 4px;
    font-size: 75%;
}

.round img {
    border-radius: 100%;
}

.label-info {
    background-color: #1976d2;
}

.label-success {
    background-color: green;
}

.label-danger {
    background-color: #ef5350;
}

.action-icons a {
    padding-left: 7px;
    vertical-align: middle;
    color: #99abb4;
}

.action-icons a:hover {
    color: #1976d2;
}

.mt-100 {
    margin-top: 10px
}

.mb-100 {
    margin-bottom: 100px
}

.m-b-5 {
  text-align: left;
}
h5{
  text-align: left;
}

#tal{
  position: relative;
  right: 350px;
  
}

.label{
  text-align: left;
}

</style>