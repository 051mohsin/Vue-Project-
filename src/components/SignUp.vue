<template>
  <v-app id="inspire">
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row justify="center">
          <v-col cols="12" sm="6">
            <v-card >
              
                      <v-card-text class="mt-12">
                        <h1 class="text-center display-2 teal--text text--accent-3"> Please Create a Account</h1>
                        
                        <h4 class="text-center mt-4">Ensure your email for registration</h4>
                        <v-form>
                          <v-row>
                            <v-container fluid>
                              <v-col cols="12" sm="4">
                            <v-text-field label=" First Name" name="fname" type="text" color="teal accent-3" />
                          </v-col>
                          <v-col cols="12" md="5">
                            <v-text-field label=" First Name" name="fname" type="text" color="teal accent-3" />
                          </v-col>
                            </v-container>
                          </v-row>
                        </v-form>
                        <h3 class="text-center mt-4">Forgot your password ?</h3>
                      </v-card-text>
                      <div class="text-center mb-5">
                        <v-btn rounded color="teal accent-3" dark>SIGN IN</v-btn>
                      </div>
                    
                
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>



<script>
export default {
  data: () => ({
    valid: true,


    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
    ],
    password: '',
    passwordrules: [
      value => !!value || " Password is required.",
      v => (v && v.length >= 8) || "Min 8 characters"
    ]
  }),

  methods: {
    // validate () {
    //   this.$refs.form.validate()
    // },
    // // reset () {
    // //   this.$refs.form.reset()
    // // },
    // resetValidation () {
    //   this.$refs.form.resetValidation()
    // },
  },
}
</script>