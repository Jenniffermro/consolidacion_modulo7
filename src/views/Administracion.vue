<template>
<v-container>
  <v-row>
<v-simple-table>
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">Curso</th>
          <th class="text-left">Cupos</th>
          <th class="text-left">Inscritos</th>
          <th class="text-left">Duración</th>
          <th class="text-left">Costo</th>
          <th class="text-left">Terminado</th>
          <th class="text-left">Fecha</th>
          <th class="text-left">Acciones</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="curso in cursos" :key="curso.id">
          <td>{{ curso.nombre }}</td>
          <td>{{ curso.cupos }}</td>
          <td>{{ curso.inscritos }}</td>
          <td>{{ curso.duracion }}</td>
          <td>{{ curso.costo }}</td>
          <td>{{ curso.completado }}</td>
          <td>{{ curso.fecha_registro }}</td>
          <td>{{}}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
  </v-row>
  <v-row>
    <div>
    <v-alert
      dense
      outlined
      type="info"
      icon="mdi-account-multiple"
    >
      Cantidad total de alumnos permitidos: <strong>{{total_cupos}} </strong> alumnos
    </v-alert>
    <v-alert
      dense
      outlined
      type="success"
      icon="mdi-account-check"
    >
      Cantidad total de alumnos inscritos: <strong>{{total_inscritos}} </strong> alumnos
    </v-alert>
    <v-alert
      dense
      outlined
      type="warning"
      icon=" mdi-account-plus"
    >
      Cantidad total de alumnos restantes: <strong>{{total_restantes}} </strong> alumnos
    </v-alert>
    <v-alert
      dense
      outlined
      type="error"
      icon=" mdi-block-helper"
    >
      Cantidad total de cursos terminados: <strong>{{total_terminados}} </strong> cursos
    </v-alert>
    <v-alert
      dense
      outlined
      type="info"
      icon="mdi-bell-ring"
    >
      Cantidad total de cursos activos: <strong>{{total_activo}} </strong> cursos
    </v-alert>
    <v-alert
      dense
      outlined
      type="success"
      icon="mdi-bell-ring-outline"
    >
      Cantidad total de cursos: <strong>{{total_cursos}} </strong> cursos
    </v-alert>
  </div>
  </v-row>
 
</v-container>



  
</template>

<script>
import { mapGetters } from 'vuex';
export default {
  name: "component-name",
  // props: {},
  data: function () {
    return {
      cursos: [
        {
          nombre: 'JavaScript Avanzado', 
          costo: 30000,
          duracion: '2 meses', 
          cupos: 20, 
          inscritos: 10, 
          completado: false,
          fecha_registro: '06/03/2022', 
        },
        {
         nombre: 'CSS para principiantes',
        costo: 10000, 
        duracion: '1 mes', 
        cupos: 35, 
        inscritos: 23,
        completado: false, 
        fecha_registro: '05/03/2022',
        },
        {
          nombre: 'JavaScript Básico de 0 a 100', 
        costo: 20000, 
        duracion: '2 meses', 
        cupos: 25,
        inscritos: 0, 
        completado: true, 
        fecha_registro: '05/03/2022',
        },
        {
          nombre:'HTML Básico', 
        costo: 10000, 
        duracion: '1 mes', 
        cupos: 35, 
        inscritos:0, 
        completado: true, 
        fecha_registro: '31/01/2022', 
        },
        {
          nombre: 'Vue JS de 0 a 100', 
        costo: 85500, 
        duracion: '5 meses', 
        cupos: 35, 
        inscritos: 35, 
        completado: false, 
        fecha_registro: '06/03/2022', 
        },
        {
          nombre: 'Estilos con SASS', 
        costo: 45000, 
        duracion: '1 mes', 
        cupos: 40, 
        inscritos: 35, 
        completado: false, 
        fecha_registro: '06/03/2022',
        },
        
      ],
    };
  },
  computed: {
    ...mapGetters(['total_cupos','total_inscritos', 'total_restantes', 'total_terminados', 'total_activo', 'total_cursos'])
    
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