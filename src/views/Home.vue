<template>
<v-app>
  <v-container>
    <v-row> 
      <v-col><v-img
  lazy-src="https://picsum.photos/id/11/10/6"
  max-height="5001"
  max-width="20000"
  src="@/assets/background.png"
></v-img></v-col>
    
    </v-row>
    
    <v-row>

    <v-col class="text-h3">Get Back to Living</v-col>

    </v-row>
    <v-row>
      <v-col class="text-h6">
        Cyzplamovir should be available to everyone who needs it.Can't Affort it ?Enroll here to seeif we can help.
      </v-col>
    </v-row>
    <v-row>
      <v-col class="smargin">
        <v-row>
          <v-col>
           <v-text-field
           v-model="Firstname"
            label="First Name"
            placeholder="Enter your Name"
            outlined
          ></v-text-field>
          </v-col>
          <v-col>
            <v-text-field
            v-model="Lastname"
            label="Last Name"
            placeholder="Afcorse last name"
            height="50"
            outlined
          ></v-text-field>
          </v-col>

        </v-row>
        <v-row>
         <v-col><v-text-field
         v-model="Address1"
            label="Address 1"
            placeholder="rahta kidhar hai"
            outlined
          ></v-text-field></v-col>

        </v-row>
        <v-row>
          <v-col><v-text-field
          v-model="Address2"
            label="Address 2"
            placeholder="Kafi lamba hai to yaha likh"
            outlined
          ></v-text-field></v-col>
          </v-row>  
          <v-row>
            <v-col>
              <v-text-field
              v-model="City"
            label="City"
            placeholder="City kya hai?"
            outlined
          ></v-text-field>
            </v-col>
            <v-col><v-select
            v-model="State"
          :items="items"
          label="State"
          outlined
        ></v-select></v-col>
            <v-col><v-text-field
            v-model="Zipcode"
            label="Zip Code"
            placeholder="Zip code"
            outlined
          ></v-text-field></v-col>
            </v-row>  
            <v-row>
              <v-col><v-text-field
              v-model="Email"
            label="E-mail"
            placeholder="E-mail"
            outlined
          ></v-text-field></v-col>
              </v-row>   
        </v-col>
        <v-col class="Enroll">

           
        <v-row>
          <v-col><i class="fa fa-lock place-right" style="font-size:36px"></i></v-col>
          <v-col><v-btn
      depressed
      :disabled="Koyal" x-large @click="navigateResponse" >Enroll</v-btn>

    </v-col></v-row>
        <v-row><v-col class="placeQ">Questions?<a><u>Talk</u> with us</a></v-col>
        </v-row>
        </v-col>
     
    </v-row>

  </v-container>
</v-app>
</template>
<style scoped>
.place-right{
  float: right;

}
.placeQ{
  margin-left: 40%;
}
.Enroll{
  margin-top: 10%;
  font-size: 30px;
}
</style>
<style>
</style>

<script>
// import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  // components: {
  //   HelloWorld,
  // },

  data(){
    return { 
    items:["Maharashtra","Chenai","Tamilnadu","Rajastha","Punjab","Gujarat"],
    Firstname:"",
    Lastname:"",
    Address1:"",
    Address2:"",
    City:"",
    State:"",
    Zipcode:"",
    Email:"",
    
}
  },
  computed:{
    Koyal(){
      if (this.Firstname.length >0 && this.Lastname.length >0 && this.Address1.length >0 && this.City.length>0 && this.State.length> 0 && this.Zipcode.length>0 && this.Email.length >0
      )
    return false
    else {
      return true
    }

    }
  },
  methods:{
    navigateResponse(){
      this.$router.push({name:'About'})
    }
  }


};
</script>
