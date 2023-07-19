<template>
  <v-container>
    <v-row>
      <CardHome-comp/>
    </v-row>
  </v-container>
</template>

<script>
  import CardHome from '@/components/CardHome.vue'

  export default {
    name: 'Home-view',

    components: {
      'CardHome-comp':CardHome,
    },
  }
</script>
