<template>
  <v-sheet
    class="mx-auto"
    elevation="8"
    max-width="1200"
  >
    <v-slide-group
      class="pa-4"
      selected-class="bg-success"
      show-arrows
    >
      <v-slide-group-item v-for="(item, index) in items" :key="index">
        <v-card class="serviceCard ml-6 mr-6" width="300">
                        <v-card-title class="titleCard title-center">{{ item.title }}</v-card-title>
        </v-card>
      </v-slide-group-item>
    </v-slide-group>
  </v-sheet>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
            title: 'Service 1',
            description: 'Descubre la hora exacta de tu nacimiento con nuestra ayuda. ¡Tu vida tiene una marca única en el tiempo, y nosotros te ayudamos a encontrarla!',
            image: '/img/relojAstral.jpg',
        },
        {
            title: 'Service 2',
            description: '',
            image: '',
        },
        {
            title: 'Service 3',
            description: 'Desvela tu esencia y destino a través de la lectura de tu carta natal. Interpretamos los misterios celestiales para ayudarte a recordar el propósito de tu vida.',
            image: '/img/lecturaNatal.jpg',
        },
        {
            title: 'Service 4',
            description: 'Explora lo que los astros dicen en este momento de tu vida con nuestra lectura transitada. Descubre la influencia cósmica en tu presente.',
            image: '/img/transitada.jpg',
        },
        {        
            title: 'Service 5',
            description: '',
            image: '',
        },
        {
            title: 'Service 6',
            description: '¿Cambiar de trabajo? ¿Estudiar una carrera? ¿Mudarse? Las estrellas tienen respuestas. Obtén orientación celestial para decisiones importantes en tu vida.',
            image: '/img/respuestas.jpg',
        },
      ],
    };
  },
  methods: {

  },
};
</script>

<style scoped>
    .serviceCard{
        background-color: gray;
        max-width: 300px;
        min-height: 350px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .titleCard{
        color: white;
        font-size: 2rem;
        font-weight: 1000;
        text-align: center;
        margin: 0;
    }
    @media screen and (max-width: 1216px) {
        .serviceCard {
            background-color: gray;
            max-width: 300px;
            min-height: 350px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-left: 6rem !important;
            margin-right: 6rem !important;
        }
    }
        @media screen and (max-width: 1080px) {
        .serviceCard {
            background-color: gray;
            max-width: 300px;
            min-height: 350px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-left: 18rem !important;
            margin-right: 18rem !important;
        }
    }
</style>