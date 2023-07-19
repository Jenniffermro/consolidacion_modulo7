<template>
    <v-container>
    <v-row justify="space-around" >
     
      <v-card v-for="curso in cursos" :key="curso.id"
        class="mx-auto"
        width="300px" >
        
         <v-img
         width="300px"
          height="400px"
          :src="curso.img"
        ></v-img>

         <v-card-title>
      {{curso.nombre}}
      </v-card-title>

          <v-app-bar
            flat
            color="rgba(0, 0, 0, 0)"
          >
            <v-app-bar-nav-icon color="white"></v-app-bar-nav-icon>

            <v-spacer></v-spacer>

            <v-btn
              color="white"
              icon
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-app-bar>

          <!-- <v-card-title class="white--text mt-8">
            <v-avatar size="56">
              <img
                alt="user"
                src="https://cdn.pixabay.com/photo/2020/06/24/19/12/cabbage-5337431_1280.jpg"
              >
            </v-avatar>
            <p class="ml-3">
              John Doe
            </p>
          </v-card-title>
        </v-img> -->

        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2">
            Información
          </div>

          <v-timeline
            align-top
            dense
          >
            <v-timeline-item>
             <div>
                <div class="font-weight-normal">
                  <strong>Costo:</strong>{{curso.costo}}
                  <strong>Duración:</strong> {{curso.duracion}}
                </div>
              </div>  
            </v-timeline-item>

            <v-timeline-item>
              <div>
                  <div class="font-weight-normal">
                  <strong>Cupos:</strong> {{curso.cupos}}
                  <strong>Completado:</strong>{{curso.completado}}
                  </div>
              </div>
            </v-timeline-item>

            <v-timeline-item>
              <div>
                <div class="font-weight-normal">
                  <strong>Fecha de registro:</strong> {{curso.fecha_registro}}
                  <strong>Descripción:</strong>{{curso.descripcion}}
                </div>
              </div>
              
            </v-timeline-item>
          </v-timeline>
        </v-card-text>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "CardHome-comp",
  // props: {},
  data: function () {
    return {};
  },
  computed: {
    ...mapState(["cursos"]),
  },
  //methods: {}
  // watch: {},
  // components: {},
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
};
</script>

<style scoped>
</style>