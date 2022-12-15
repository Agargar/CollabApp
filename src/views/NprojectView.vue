<template>
  <div class = "container mt-5">
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
       <b-form-group id="input-group-1" label="Nom :" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.nn"
          placeholder="...."
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Description :" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          placeholder="...."
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Compétence:" label-for="input-3">
        <b-form-select
          id="input-3"
          v-model="form.food"
          :options="foods"
          required
        ></b-form-select>
      </b-form-group>

      <b-form-group id="input-group-4" v-slot="{ ariaDescribedby }">
        <b-form-checkbox-group
          v-model="form.checked"
          id="checkboxes-4"
          :aria-describedby="ariaDescribedby"
        >
          <b-form-checkbox value="me">Privée</b-form-checkbox>
          <b-form-checkbox value="that">Public</b-form-checkbox>
        </b-form-checkbox-group>
      </b-form-group>

      <b-button type="submit" variant="primary">Publier</b-button>
      <b-button type="reset" variant="danger">Effacer</b-button>
    </b-form>

    <div class="col-md-6 col-lg-7 col-md-offset-3">
    <div class="panel panel-default chat-widget">
    <div class="panel-heading">
      <h3 class="panel-title"><i class="fa fa-comments"></i> Chat</h3>
    </div>
    <div class="panel-body">
      <div class="message">
          <div class="avatar">
          <img class="img-circle avatar" alt="chat avatar" src="https://bootdey.com/img/Content/avatar/avatar1.png">
          </div>
          <div class="message-text-wrapper">
            <div class="message-text">
              Basic panel example awesome one bewsom Basic panel example awesome
            </div>
          </div>
          <p class="time-stamp"><i class="fa fa-check"></i> 5 minute ago</p>
      </div>

      <div class="message message-right">
          <div class="avatar">
          <img class="img-circle avatar" alt="chat avatar" src="https://bootdey.com/img/Content/avatar/avatar2.png">
          </div>
          <div class="message-text-wrapper">
            <div class="message-text">
              Basic panel example awesome one bewsom Basic panel example awesome
            </div>
          </div>
          <p class="time-stamp"><i class="fa fa-check"></i> 2 minute ago</p>
      </div>

      <div class="message">
          <div class="avatar">
          <img class="img-circle avatar" alt="chat avatar" src="https://bootdey.com/img/Content/avatar/avatar1.png">
          </div>
          <div class="message-text-wrapper">
            <div class="message-text">
              <a href="#" title="Singapore cityscape" data-gallery="">
              <img src="https://via.placeholder.com/200x320/" alt="singapore pic"></a>
            </div>
          </div>
          <p class="time-stamp"><i class="fa fa-check"></i> 1 minute ago</p>
      </div>

      <div class="message message-right">
          <div class="avatar">
          <img class="img-circle avatar" alt="chat avatar" src="https://bootdey.com/img/Content/avatar/avatar2.png">
          </div>
          <div class="message-text-wrapper">
            <div class="message-text">
              Basic panel example awesome one bewsom Basic panel example awesome
            </div>
          </div>
          <p class="time-stamp"><i class="fa fa-check"></i> Now</p>
      </div>
      </div>
      <div class="panel-footer">
        <div class="avatar">
          <img class="img-circle avatar" alt="chat avatar" src="https://bootdey.com/img/Content/avatar/avatar1.png">
        </div>
        <div class="input-group">
        <input type="text" placeholder="Press Enter" class="form-control primary">
        <span class="input-group-btn">
            <button class="btn btn-primary" type="button">Send</button>
        </span>
      </div>
      </div>
  </div>
</div>
  
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          nn: '',
          name: '',
          food: null,
          checked: []
        },
        foods: [{ text: 'Select One', value: null }, 'Dev Front', 'Dev Backend', 'Ui Designer', 'character designer'],
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(event) {
        event.preventDefault()
        // Reset our form values
        this.form.nn = ''
        this.form.name = ''
        this.form.food = null
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = false
        })
      }
    }
  }
</script>

<style>
#app {
  text-align: left;

}

.label {
  position: relative;
  text-align: left;
}

.input-group-1 {
  text-align: left;
}
.chat-widget{
    -webkit-box-shadow: 0 2px 2px 0 rgba(0,0,0,0.2),0 6px 10px 0 rgba(0,0,0,0.3);
    box-shadow: 0 2px 2px 0 rgba(0,0,0,0.2),0 6px 10px 0 rgba(0,0,0,0.3);
}

.panel-default > .panel-heading {
    color: #333;
    background-color: #fcfcfc;
    border-color: #ddd;
    border-color: rgba(221,221,221,0.85);
}

/*Chat widget*/
.chat-widget .message {
    display:block;
	margin-bottom:20px;
    
}

.chat-widget .message .avatar {
	width:55px;
	float:left;
    
}

.chat-widget .message.message-right .avatar {
	width:55px;
	float:right;
}

.chat-widget .avatar img {
	height:40px;
	width:40px!important;
}

.chat-widget .message .message-text-wrapper {
	display:table-cell;
	width:1%;
}

.chat-widget .message .message-text {
	padding:15px;
	border-radius:4px;
	border:1px solid #ddd;
	border:1px solid rgba(221,221,221,0.68);
	position:relative;
	width:100%;
    -webkit-box-shadow: 0 1px 4px 0 rgba(0,0,0,0.37);
    box-shadow: 0 1px 4px 0 rgba(0,0,0,0.37);
}

.chat-widget .message.message-right .message-text {
	background:#fbfbfb;
}

.chat-widget .message .message-text img {
	width:200px;
	height:150px;
}

.chat-widget .message .time-stamp {
	margin-left:55px;
}

.chat-widget .message.message-right .time-stamp {
	margin-left:0;
	margin-right:55px;
	display:block;
	text-align:right;
}

.chat-widget .message .message-text:before,.chat-widget .message .message-text:after {
	right:100%;
	top:30px;
	border:solid transparent;
	content:" ";
	height:0;
	width:0;
	position:absolute;
	pointer-events:none;
}

.chat-widget .message .message-text:before {
	border-color:rgba(0,0,0,0);
	border-right-color:#ddd;
	border-width:10px;
	margin-top:-19px;
}

.chat-widget .message .message-text:after {
	border-color:rgba(213,71,28,0);
	border-right-color:#fff;
	border-width:9px;
	margin-top:-18px;
}

.chat-widget .message.message-right .message-text:before,.chat-widget .message.message-right .message-text:after {
	left:100%;
	top:30px;
	border:solid transparent;
	content:" ";
	height:0;
	width:0;
	position:absolute;
	pointer-events:none;
}

.chat-widget .message.message-right .message-text:before {
	border-color:rgba(0,0,0,0);
	border-left-color:#ddd;
	border-width:10px;
	margin-top:-19px;
}

.chat-widget .message.message-right .message-text:after {
	border-left-color:#fbfbfb;
	border-width:9px;
	margin-top:-18px;
}

.chat-widget .panel-footer {
	border:none;
	background:transparent;
	margin-top:-20px;
}

.chat-widget .panel-footer .avatar {
	width:55px;
	float:left;
	margin-top:-2px;
}

@media (max-width:767px) {
	label.margin {
		margin-top:25px;
		margin-bottom:15px;
	}
}

</style>