<template>
    <v-carousel class="serviceCarrousel">
      <v-carousel-item v-for="(item, index) in items" :key="index">
        <v-row>
          <v-col class="left d-flex flex-column align-center">
            <v-card class="serviceCard">
              <div class="d-flex flex-column align-center">
                <v-img class="imageCarousel" :src="item.leftImage" width="400" height="200"></v-img>
              </div>
              <v-card-title class="titleCard">{{ item.leftTitle }}</v-card-title>
              <v-card-text class="descriptionCard">{{ item.leftDescription }}</v-card-text>
              <div class="d-flex flex-column align-center">
                <v-btn class="seeMore" @click="verMasClick(index)">Ver más</v-btn>
              </div>
            </v-card>
          </v-col>
          <v-col class="right d-flex flex-column align-center">
            <v-card class="serviceCard">
              <div class="d-flex flex-column align-center">
                <v-img class="imageCarousel" :src="item.rightImage" width="400" height="200"></v-img>
              </div>
              <v-card-title class="titleCard">{{ item.rightTitle }}</v-card-title>
              <v-card-text class="descriptionCard">{{ item.rightDescription }}</v-card-text>
              <div class="d-flex flex-column align-center">
                <v-btn class="seeMore" @click="verMasClick(index)">Ver más</v-btn>
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-carousel-item>
    </v-carousel>
  </template>
  
  <script setup>
  const items = [
    {
      leftTitle: 'Corrección Horaria',
      leftDescription: 'Descubre la hora exacta de tu nacimiento con nuestra ayuda. ¡Tu vida tiene una marca única en el tiempo, y nosotros te ayudamos a encontrarla!',
      leftImage: '/img/relojAstral.jpg',

      rightTitle: 'Lectura Carta Natal',
      rightDescription: 'Desvela tu esencia y destino a través de la lectura de tu carta natal. Interpretamos los misterios celestiales para ayudarte a recordar el propósito de tu vida.',
      rightImage: '/img/lecturaNatal.jpg',
    },
    {
      leftTitle: 'Carta Transitada',
      leftDescription: 'Explora lo que los astros dicen en este momento de tu vida con nuestra lectura transitada. Descubre la influencia cósmica en tu presente.',
      leftImage: '/img/transitada.jpg',

      rightTitle: 'Respuestas Concretas',
      rightDescription: '¿Cambiar de trabajo? ¿Estudiar una carrera? ¿Mudarse? Las estrellas tienen respuestas. Obtén orientación celestial para decisiones importantes en tu vida.',
      rightImage: '/img/respuestas.jpg',
    },
  ];
  const verMasClick = (index) => {
    console.log(index);
  };
  </script>

<style scoped>

.serviceCarrousel{
  height: 450px !important;
}
.v-carousel-item {
    padding-left: 5.5rem;
    margin-bottom: 0 !important;
}
.serviceCard{
  background-color: beige;
  width: 400px;
  height: 410px;
}
.titleCard{
  color: rgb(100, 99, 94);
  font-size: 2rem;
  font-weight: 900;
}
.descriptionCard{
  color: rgb(97, 94, 84);
  font-size: 1.2rem;
  font-weight: 500;
}
.text-col{
    margin-top: 2rem;
}
.imageCarousel {
    background-color: rgb(83, 80, 73);
    /* margin-top: 1rem; */
}
.seeMore {
  margin-top: 10px; /* Espacio entre el texto y el botón "Ver más" */
  background-color: rgb(83, 80, 73);
  color: beige;
  font-size: 1.2rem;
  font-weight: 500;
  margin-top: 0.8rem;
}

div.v-col.right{
  margin-right: 96px;
}
</style>

<style>
.serviceCarrousel .v-carousel__controls {
    align-items: center;
    bottom: 0;
    display: none;
    height: 50px;
    justify-content: center;
    list-style-type: none;
    position: absolute;
    width: 100%;
    z-index: 1;
    margin-bottom: 10px;
}
</style>