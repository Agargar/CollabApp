<template>
  <div class="container">
    <div class="box">
      <b-form>
        <!--Full name-->

        <b-form-input
          type="text"
          id="first"
          v-model="text"
          placeholder="First Name"
        ></b-form-input>
        <b-form-input
          type="text"
          id="second"
          v-model="text"
          placeholder="Last Name"
        ></b-form-input>
        <!--Email-->
        <div v-if="error" class="alert alert-danger" role="alert">
          {{ error }}
        </div>

        <b-alert
          class="err"
          v-model="showDismissibleAlert"
          variant="danger"
          dismissible
        >
          {{ errorspe }}
        </b-alert>
        <b-form @submit.stop.prevent>
          <div class="help">
            <b-form-input
              @keyup.enter="login()"
              @keypress="validate()"
              v-model="userId"
              :state="validation"
              type="email"
              id="username"
              placeholder="Email"
            ></b-form-input>
            <b-button
              class="forms"
              v-b-popover.hover.right="
                'Email must be between 7 & 30 letters and cannot contain /:*?<>|'
              "
              variant="primary"
              >?</b-button
            >
          </div>
        </b-form>
        <!--Password-->
        <b-form @submit.stop.prevent>
          <div class="help">
            <b-form-input
              @keyup.enter="login()"
              v-model="pass"
              :state="validationPass"
              type="password"
              id="password"
              aria-describedby="password-help-block"
              placeholder="Password"
            ></b-form-input>
            <b-button
              class="forms"
              v-b-popover.hover.right="'Password can\'t be less than 8 letters'"
              >?</b-button
            >
          </div>
        </b-form>

        <!--button-->
        <div v-if="erroreg" class="alert alert-danger" role="alert">
          {{ erroreg }}
        </div>
        <b-button class="log" variant="primary" @click="register()"
          >Sign up</b-button
        >
      </b-form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userId: "",
      first: "",
      second: "",
      password: "",
      username: "",
      pass: "",
      showDismissibleAlert: false,
      errorspe: false,
      erroreg: false,
    };
  },
  methods: {
    register() {
      username = document.getElementById("username").value;
      password = document.getElementById("password").value;
      first = document.getElementById("first").value;
      second = document.getElementById("second").value;
      if (
        username.length < 7 ||
        password.length < 7 ||
        first == "" ||
        second == ""
      ) {
        this.erroreg = "Invalid/missing input";
      } else {
        window.location.href = "/HomeView"; // Redirecting to other page.
      }
    },
    validate() {
      const input = document.getElementById("username");
      const errorspe = document.getElementById("errorspe");
      const regex = /[\\\/:*?"<>|]+/;
      input.addEventListener("input", (e) => {
        const value = e.target.value;

        if (regex.test(value)) {
          input.value = value.slice(0, value.length - 1);
          this.showDismissibleAlert = true;
          this.errorspe = 'Cannot contain: /:*?"<>|';
        } else {
        }
      });
    },
  },
  computed: {
    validation() {
      return this.userId.length > 4 && this.userId.length < 40;
    },
    validationPass() {
      return this.pass.length > 7 && this.pass.length < 40;
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
}

.box {
  width: 90%;
  max-width: 350px;
  height: 500px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: url(../assets/images/wave.png) ;
  background-repeat: no-repeat;
  background-color: #FFD700;
  
  padding: 50px 60px 70px;
  text-align: center;
  border-radius: 2px;
}
input {
  display: flex;
  height: 20px;
}

.help {
  display: flex;
  background: none;
  border: none;
  width: 100%;
  /*transform: translate(-5%, 58px);*/
}

#first {
  margin: 27px 0;
  display: flex;
  align-items: center;
  height: 50px;
  width: 100%;
  border: 0;
  border-radius: 2px;
  outline: 0;
  padding: 18px 15px;
}
#second {
  margin: 12px 0;
  display: flex;
  align-items: center;
  height: 50px;
  width: 100%;
  border: 0;
  border-radius: 2px;
  outline: 0;
  padding: 18px 15px;
}
#username {
  margin: 15px 0;
  display: flex;
  align-items: center;
  height: 50px;
  width: 100%;
  border: 0;
  border-radius: 2px;
  outline: 0;
  padding: 18px 15px;
  margin-right: -65px;
}
#password {
  margin: 15px 0;
  display: flex;
  align-items: center;
  height: 50px;
  width: 100%;
  border: 0;
  border-radius: 2px;
  outline: 0;
  padding: 18px 15px;
  margin-right: -65px;
}

#error {
  margin-bottom: 15px;
}


.log {
  background: black;
  border: none;
  border-radius: 2px;
  width: 50%;
  margin-top: 25px;
}
.log:hover{
  background: #fff;
  color: #000000;
}
.log:active{
  background-color:  #fff;
  color:#000000;
}
.err {
  padding: none none;
  padding-right: 0;
  border-radius: 2px;
  margin-top: 20px;
}
:deep(.close) {
  border-radius: 0;
  background: #f8d7da;
  border: none;
}
.forms {
  display: inline-block;
  background: none;
  border: none;
  transition: none;
  transform: translate(30px, 13px);
  color: transparent;
  height: 50px;
}
.forms:hover {
  color: transparent;
  background: none;
  cursor: default;
}
.forms:active {
  color: transparent;
  border: none;
  background: transparent;
  border-color: transparent;
}
</style>