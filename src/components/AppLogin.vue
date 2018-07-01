<template>
    <v-container>
            <v-alert :value="alert" color="lime" type="warning" >
                Please fill email and password
            </v-alert>
        <v-form @submit.prevent="submit">
            <v-text-field
            v-model="email"
            label="E-mail"
            required
            ></v-text-field>
            <v-text-field
            label="Password"
            v-model="password"
            type="password"
            required
            ></v-text-field>            
            <v-btn class="green" type="submit">Submit</v-btn>
        </v-form>
    </v-container>
</template>

<script>
  export default {
    data(){
        return{
            email:null,
            password:null,
            alert:false
        }
    },
    methods:{
        submit(){
            if(!this.email && !this.password){
                this.alert = true;
            }
            console.log(`Email is ${this.email} and Password is ${this.password}`);
        }
    }
    // () => ({
    //   valid: false,
    //   name: '',
    //   nameRules: [
    //     v => !!v || 'Name is required',
    //     v => v.length <= 10 || 'Name must be less than 10 characters'
    //   ],
    //   email: '',
    //   emailRules: [
    //     v => !!v || 'E-mail is required',
    //     v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
    //   ]
    // })
  }
</script>