<template>
    <div>
    <v-app-bar
      color="deep-purple accent-4"
      dense
      dark
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Cursos AlfaWeb</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon to="/">
        <v-icon>mdi-home-variant</v-icon>
      </v-btn>

      <v-btn icon to="/administracion">
        <v-icon> mdi-yeast</v-icon>
      </v-btn>

      
    </v-app-bar>
  </div>
</template>

<script>
export default {
    name: 'Navbar-comp',
    // props: {},
    data: function(){
        return {
          drawer: false,
          group: null,
          routes: [
            {
              icon: "mdi-home-variant",
              title: "Inicio",
              name: "Home",
            },
            {
              icon: "mdi-yeast",
              title: "Administracion",
              name: "Administracion",
            }
          ]
        }
    },
    // computed: {},
    //methods: {}
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
    
</style>