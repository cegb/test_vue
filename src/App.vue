<template>
  <div id="app">
    <v-toolbar color="primary">
      <v-toolbar-side-icon></v-toolbar-side-icon>
      <v-toolbar-title>Mi App</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat>Inicio</v-btn>
        <v-btn flat>Buscar</v-btn>
        <v-btn flat>Acerca de</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-container grid-list-md>
      <v-layout row wrap>
        <v-flex
          xs4
          v-for="(personaje, index) in personajes"
          :key="index"
          class="mb-2">
          <v-card>
            <v-img :src="personaje.imagen"></v-img>
            <v-card-title primary-title>
              <h3 class="headline mb-0">{{ personaje.nombre }}</h3>
            </v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      personajes: [
        {
          id: 1,
          nombre: 'Morty',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
        },
        {
          id: 2,
          nombre: 'Rick',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {
          id: 3,
          nombre: 'Summer',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
        },
        {
          id: 4,
          nombre: 'Beth',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
        },
        {
          id: 5,
          nombre: 'Jerry',
          imagen: 'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
        }
      ]
    }
  }
}
</script>
