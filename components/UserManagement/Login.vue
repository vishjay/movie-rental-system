
<template>
  <div>
    <b-container>
    <b-card title="Login"  class="col-md-6 mx-auto wrapper-card"> 
      <b-form @submit="userLogin" >
        <b-form-group
                id="input-group-1"
                label="Email address:"
                label-for="input-1"
              >
        <b-form-input
          id="input-1"
          type="email"
          placeholder="Enter email"
          v-model="login.Email"
        ></b-form-input>
        </b-form-group>
        <b-form-group>
            <label for="text-password">Password</label>
            <b-input type="password" id="text-password" aria-describedby="password-help-block" v-model="login.Password"></b-input>
        </b-form-group>
        <b-button type="submit" block variant="outline-info">Login</b-button>
      </b-form>
    </b-card>
    </b-container>
  </div>
</template>

<script>
export default {
    data() {
    return {
      login: {
        Email: '',
        Password: ''
      }
    }
  },
  methods: {
    async userLogin(e) {
      e.preventDefault();
      try {
        let response = await this.$auth.loginWith('local', { data: this.login })
        console.log(response)
        console.log(this.$auth)
        this.$router.push('/')
      } catch (err) {
        console.log(err)
      }
    }
  }
}
</script>
<style>
.wrapper-card {
  margin-top: 20px;
  padding-bottom: 20px;
}
</style>