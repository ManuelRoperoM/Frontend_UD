<template>
    <v-container>
      <v-row justify="center">
        <v-col v-for="(element, index) in testimonials" :key="index" class="column" cols="auto">
            <v-card class="testimonialCard mx-auto" max-width="344">
                <div class="testimonialContent">
                    <v-avatar size="90" class="ml-2 mt-2">
                        <v-img
                            :src='element.photo'
                            alt="John"
                        ></v-img>
                    </v-avatar>
                    <div class="contentInfo">
                        <v-card-title>{{ element.author }}</v-card-title>
                        <v-card-subtitle>{{ element.signal }}</v-card-subtitle>
                    </div>
                </div>
            <v-card-text>{{ element.content }}</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    data() {
      return {
        testimonials: [
          { content: "¡Excelente servicio! Realmente superó mis expectativas.", author: "Lionel Messi", signal: "Acuario, 22 años",photo:"/img/Perfil/messi.jpeg" },
          { content: "Estoy muy satisfecho con el servicio. ¡Altamente recomendado!", author: "Michael Jordan", signal: "Libra, 54 años",photo:"/img/Perfil/jordan.jpeg" },
          { content: "El equipo de soporte fue muy amable y resolvió mi problema rápidamente.", author: "Marge Simpson", signal: "Piscis, 38 años",photo:"/img/Perfil/Marge.jpg"},
          { content: "Increíble experiencia. ¡Definitivamente volveré a consultar!", author: "Coco Chanel", signal: "Tauro, 19 años",photo:"/img/Perfil/coco-chanel.jpg"},
          { content: "¡Lo recomiendo encarecidamente a todos mis amigos y familiares!", author: "Rick Sanchez", signal: "Aries, 29 años",photo:"/img/Perfil/rick.jpg" },
          { content: "Increíble experiencia con este servicio.", author: "Son Goku", signal: "Capricorino, 45 años",photo:"/img/Perfil/goku.jpg" },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .container{
    background-color: blue
  }
  /* .column{
    background-color: red !important;
  } */
  .testimonialCard {
    max-height: 160px; /* Ajusta la altura según tus preferencias */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .testimonialContent {
    display: flex;
    align-items: center;
  }
  </style>