<template>   
    <v-card
    max-width="400"
    class="mx-auto mt-12"
    >
        <v-card-title>Please enter your credentials</v-card-title>
        
        <v-card-text>
            <v-text-field
                label="User"
                outlined
                v-model="user"
            ></v-text-field>

            <v-text-field
                label="Password"
                outlined
                :type="'password'"
                v-model="password"
            ></v-text-field>
        </v-card-text>

        <v-card-actions>            
                <v-btn text @click="authenticate">Login</v-btn>
                <v-spacer></v-spacer>       
                <v-btn text @click="cancel">Cancel</v-btn>            
        </v-card-actions>
    </v-card>   
</template>

<script>
    export default({
        
        data: function () {
           return{
               user: '',
               password: '',
           }
        },
        methods: {
            authenticate(){
                alert(this.user +" "+ this.password);
            },
            cancel(){
                this.user='';
                this.password='';
            }
        }
        
    })
</script>

<style scoped>

</style>