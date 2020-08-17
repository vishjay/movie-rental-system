
<template>
  <div>
    <b-container>
    <b-card title="Register"  class="col-md-6 mx-auto wrapper-card"> 
      <b-form>
        <b-form-group id="input-group-1" label="First Name:" label-for="input-1">
        <b-form-input
          id="input-1"
          required
          placeholder="Enter name"
        ></b-form-input>
        </b-form-group>
        <b-form-group id="input-group-2" label="Last Name:" label-for="input-2">
        <b-form-input
          id="input-2"
          required
          placeholder="Enter name"
        ></b-form-input>
        </b-form-group>
        <b-form-group
                id="input-group-3"
                label="Email Address:"
                label-for="input-3"
              >
        <b-form-input
          id="input-3"
          type="email"
          required
          placeholder="Enter email"
        ></b-form-input>
        </b-form-group>
        <b-form-group>
        <label for="text-password">Password</label>
        <b-input type="password" id="text-password" aria-describedby="password-help-block"></b-input>
        </b-form-group>
        <b-button block variant="outline-info">Login</b-button>
      </b-form>
    </b-card>
    </b-container>
  </div>
</template>

<script>
export default {}
</script>
<style>
.wrapper-card {
  margin-top: 20px;
  padding-bottom: 20px;
}
</style>
