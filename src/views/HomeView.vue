<template>
  <v-app>
    <nav-bar />
    <v-container fluid>
      <v-card color="#f7f7f7" height="140px" class="d-flex align-center justify-center mt-12">
        <v-row>
          <v-col cols="12" sm="12">
            <v-item-group mandatory class="mt-n1">
              <v-container>
                <v-row justify="center" class="space">
                  <v-col cols="12" xs="12" sm="4" md="2" v-for="(category, i) in data.categories" :key="i">
                    <v-item v-slot="{ isSelected, toggle }">
                      <v-card :color="isSelected ? '#D5F0DB' : 'white'" :class="isSelected ? 'borderme' : 'borderout'"
                        class="d-flex align-center rounded-lg mx-2" height="100" @click="toggle" flat>
                        <v-row>
                          <v-col cols="12" sm="12" class="text-center">
                            <v-img class="mx-auto" :src="category.img" max-height="40" max-width="40" contain> </v-img>
                            <p :class="isSelected ? 'text-green' : 'text-black'" class="caption mt-4 text-subtitle-2">
                              {{ category.title }}
                            </p>
                          </v-col>
                        </v-row>
                      </v-card>
                    </v-item>
                  </v-col>
                </v-row>
              </v-container>
            </v-item-group>
          </v-col>
        </v-row>
      </v-card>

      <v-toolbar color="transparent" class="mt-3">
        <v-checkbox v-model="data.chair" label="Chairs" class="check mt-4"></v-checkbox>
        <v-checkbox v-model="data.other" label="Othermass" class="check mt-4"></v-checkbox>
        <v-divider vertical></v-divider>
        <v-btn variant="text">Leather Colors
          <v-icon right class="ml-2 mt-n1">fas fa-house</v-icon>
        </v-btn>
        <v-divider vertical></v-divider>
        <v-btn variant="text">Choose Design
          <v-icon right class="ml-2 mt-n1">fas fa-caret-right</v-icon>
        </v-btn>
        <v-divider vertical></v-divider>
        <span class="text-caption mx-2">Price till</span>
        <v-slider v-model="slider2" label="track-color" :min="10" :max="10000" :step="10" class="mt-5"></v-slider>
        <span class="text-caption mx-2">${{ slider2 }}</span>
      </v-toolbar>
      <v-divider></v-divider>
      <br/>
      <v-row>
        <v-col cols="12" sm="3" v-for="(chair, i) in data.chairs" :key="i">
          <v-card height="300" align="center" flat outlined tile>
            <v-img :src="chair.image" width="200" height="200" contain></v-img>
            <v-card-text class="mt-n1">
              <strong>{{ chair.title }}</strong>
            </v-card-text>
            <v-card-text class="mt-n4">
              <strong>{{ chair.price }}</strong>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-divider></v-divider>

      <v-toolbar color="transparent">
        <v-toolbar-title class="text-caption">Show more chairs</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-icon color="grey" left class="mr-4 mt-n1">fas fa-long-arrow-alt-left</v-icon>
        <span class="text-caption">3</span>
        <v-icon color="grey" left class="ml-4 mt-n1 mr-2">fas fa-long-arrow-alt-right</v-icon>
      </v-toolbar>
    </v-container>
  </v-app>

</template>

<script setup>
import NavBar from '@/components/NavBar.vue'
import { ref } from 'vue'
const slider2 = ref(9000)
let data = {
  chair: true,
  other: false,
  categories: [
    { img: "9.png", title: "SLEEPING BEDS" },
    { img: "2.png", title: "LOUNGE CHAIRS" },
    { img: "1.png", title: "CHAIRS" },
    { img: "4.png", title: "OFFICE CHAIRS" },
    { img: "8.jpg", title: "TABLES NIGHTSTANDS" },
    { img: "6.png", title: "KITCHEN FURNITURE" },
  ],
  chairs: [
    {
      class: "pa-0",
      image: "c1.jpg",
      title: "Lounge Chair",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c2.jpg",
      title: "Repos",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c3.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c4.png",
      title: "Loby Chair",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c5.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c6.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c7.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c8.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c9.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c10.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c11.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c12.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c13.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c14.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c15.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
    {
      class: "pa-0",
      image: "c16.png",
      title: "Modern Lounge",
      price: "$ 145.00",
    },
  ]
}
</script>

<style scoped>  
.v-card.borderme {
  border: 2px solid black !important;
}
.v-card.borderout {
  border: 1px solid #d5f0db !important;
}
</style>
