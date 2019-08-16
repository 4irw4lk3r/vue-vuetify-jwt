<template>
    <nav>
        <v-toolbar bottom dark flat class="amber darken-1">
            <v-toolbar-title>Hey kid! Do you wanna some movies?</v-toolbar-title>

            <v-toolbar-items>
                <v-btn text><span>home</span></v-btn>
            </v-toolbar-items>

            <v-spacer></v-spacer>
            
            <v-toolbar-items>

               <div style="margin-top: 3%">
                   <v-text-field
                        solo-inverted
                   ></v-text-field>
               </div>
               
               <v-btn icon>
                <v-icon large>mdi-arrow-right-box</v-icon>
               </v-btn>
            </v-toolbar-items>
            

            <v-spacer></v-spacer>

            <v-toolbar-items>
                <v-menu bottom
                    :offset-y="true"
                    :open-on-hover="true" 
                    :close-on-content-click="true"
                >
                    <template v-slot:activator="{ on }">
                        <v-btn depressed class="amber darken-1" v-on="on">
                            Genre
                        </v-btn>
                    </template>
                    <v-list dark class="amber darken-1">
                        <v-list-item
                        v-for="(item, index) in items"
                        :key="index"                        
                        >
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                        </v-list-item>
                    </v-list>
                </v-menu>

                <v-btn text>
                    <span>Login</span>
                    <v-icon small>mdi-login</v-icon>              
                </v-btn>
            </v-toolbar-items>
        </v-toolbar>

    </nav>
</template>

<script>
    export default {
        data: () => ({
            items: [
                { title: 'Action' },
                { title: 'Romance' },
                { title: 'Comedy' },
                { title: 'Terror' },
            ],
        })
    }
</script>

<style lang="scss" scoped>

</style>