<template>

    <div class="ctn">
    <h2>Création d'un jeu vidéo 3d open world </h2>
    <h4>Avancement du projet </h4>
      
    <b-progress :value="34" variant="primary" striped :animated="animate"></b-progress>
     
       <pre class="tab">.<i>12/09/2022</i>: Projet crée                        <strong>.</strong><i>12/09/2022</i>:<strong> @LAxer</strong> a ajouté des character                ...</pre>
 
       <div class="card-body" style="
    margin-bottom: 10px;">
                                <h2 class="card-title"><strong>Messagerie</strong></h2>
                                <hr style="height:1px;border-width:0;color:gray;background-color:gray">
                       </div>

                            <div class="comment-widgets m-b-20">

                                <div class="d-flex flex-row comment-row">
                                    <div class="p-2"><span class="round"><img src="https://i.imgur.com/uIgDDDd.jpg" alt="user" width="50"></span></div>
                                    <div class="comment-text w-100">
                                        <h5 >@Gogzila </h5>
                                        
                                        <div class="comment-footer">
                                            
                                        </div>
                                        <img class="m-b-5 m-t-10" src="@/assets/bledner3d.png" alt="Blender3d" width="300" height="250">
                                    </div>
                                </div>

                                <div class="d-flex flex-row comment-row ">
                                    <div class="p-2"><span class="round"><img src="https://i.imgur.com/tT8rjKC.jpg" alt="user" width="50"></span></div>
                                    <div class="comment-text active w-100">
                                        <h5>@SonAF12</h5>
                                       
                                        <div class="comment-footer">
                                           
                                        </div>
                                        <img class="m-b-5 m-t-10" src="@/assets/charadesign.png" alt="Charadesign" width="550)" height="400">
                                    </div>
                                </div>

                                <div class="d-flex flex-row comment-row">
                                    <div class="p-2"><span class="round"><img src="https://i.imgur.com/cAdLHeY.jpg" alt="user" width="50"></span></div>
                                    <div class="comment-text w-100">
                                        <h5>@shh121.</h5>
                                       
                                        <div class="comment-footer">
                                           
                                        </div>
                                        <p class="m-b-5 m-t-10" style="text-align:left">Je vous envoie les sprites cce weekend.</p>
                                    </div>
                                </div>

                                <div class="bg-light p-2">
                                    <div>
                          <b-form-select v-model="selected" :options="options" style="margin-bottom: 10px;" ></b-form-select>
                          </div>
                   
                      </div>
                      <hr style="height:1px;border-width:0;color:gray;background-color:gray">
                    <div class="mt-2 text-right"><button  class="btn btn-primary btn-sm shadow-none" type="button" style="  margin-left: 83%;">Envoyer</button></div>
                    <div class="mt-3"> {{ file1 ? file1.name : '' }}</div>

<!-- Plain mode -->
<b-form-file v-model="file2" class="mt-3" plain></b-form-file>
<hr style="height:2px;border-width:0;color:gray;background-color:gray">
</div>

<pre>


            
</pre>

                </div>

                

 

</template>

<script>
  export default {
    data() {
      return {
        animate: true
      }
    }
  }
</script>

<style>
.px-2 {
  margin-left: 10px;
}
h5{
    text-align: left;
}
h2{
    font-size:x-large ;
}

h4{
    font-size: medium;
    text-align: left;
}
.ctn {
    background-color: white;
    margin-left: 10%;
    margin-right: 10%;
}
.tab {
    text-align: left;
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
.card-body{
    margin-bottom: 100px;
}


pre{
    margin-bottom: 10%;
}


</style>