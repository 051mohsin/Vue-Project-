
 <template>
  <v-app id="inspire">
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row  justify="center">
          <v-col cols="6">
            <v-card class="elevation-12">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12"  >
                      <v-card-text class="mt-12">
                        <h1
                          class="text-center display-2 teal--text text--accent-3"
                        > Please LogIn</h1>
                        <div class="text-center mt-4">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-google</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-facebook</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>mdi-linkedin</v-icon>
                          </v-btn>
                        </div>
                        <h4 class="text-center mt-4">Ensure your email for registration</h4>
                        <v-form>
                          <v-text-field
                            label="Email"
                            name="Email"
                            v-model="email"
                            :rules="emailRules"
                            type="text"
                            color="teal accent-3"
                          />
                          <v-text-field
                            id="password"
                            label="Password"
                            name="password"
                            v-model="password"
                            :rules="passwordrules"
                            type="password"
                            color="teal accent-3"
                          />
                        </v-form>
                        <h3 class="text-center mt-4">Forgot your password ?</h3>
                      </v-card-text>
                      <div class="text-center mb-5">
                        <v-btn rounded color="teal accent-3" dark>SIGN IN</v-btn>
                      </div>
                    </v-col>
                    
                  </v-row>
                </v-window-item>
                
              </v-window>
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
      password:'',
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
