<template>
  <div>
    <h1 id="headline">Logga in på ditt konto, {{this.input}} för att ladda upp ditt cv</h1>
    <div id="section" class="m-t-12">
      <div class="columns is-centered">
        <div class="column is-6">
          <div class="box">
            <div class="container">
              <b-field label="Email" type="is-danger" message="This email is invalid" id="email">
                <b-input type="email" v-model="input"></b-input>
                <span class="button is-static">@iths.se</span>
              </b-field>

              <b-field label="Password">
                <b-input type="password" value="iwantmytreasure" password-reveal></b-input>
              </b-field>

              <b-field>
                <b-input type="button" value="Sign In" @click="checkForValidEmail"></b-input>
              </b-field>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "SignIn",
  data() {
    return {
      input: ''
    };
  },
  methods: {
      checkForValidEmail(){
          console.log("before if")
          if(this.input === "hej"){
                console.log("valid")
          }
      }
  }
};
</script>
<style scoped>
/*Exempel css*/
#headline {
  color: red;
}
#loginSection{
    background-color: seagreen;
}
</style>