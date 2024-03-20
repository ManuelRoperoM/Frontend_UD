<template>
    <v-carousel>
      <v-carousel-item
        v-for="(item, index) in items"
        :key="index"
        :src="item.image"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-row align="center">
            <v-col cols="12" md="6" class="text-col">
                <h2 class="display-4">{{ item.title }}</h2>
                <p class="body-1">{{ item.description }}</p>
            </v-col>
            <v-col cols="12" md="6">
                <v-img class="imageCarousel" :src='item.astro' alt="Slide Image" width="400"></v-img>
            </v-col>
        </v-row>
      </v-carousel-item>
    </v-carousel>
</template>
<script setup>
    const items = [
    {
        title: '¡Descubre Tu Destino Estelar en Tu Carta de Nacimiento!',
        description: '¡Bienvenido a la experiencia cósmica que cambiará tu vida! ¿Alguna vez te has preguntado qué secretos esconde el universo sobre ti? Tu carta astral tiene las respuestas y estamos aquí para revelarte esos misterios celestiales.',
        astro: '/img/astLeyendo.png',
    },
    {
        title: 'Desentraña los Misterios de Tu Existencia',
        description: 'Imagina poder entender las complejidades de tu vida a través de las estrellas. Tu carta de nacimiento es como el mapa celestial que te guiará a través de los caminos de tu destino. Descubre cómo los astros influyeron en tu personalidad, tus relaciones y tus metas.',
        astro: '/img/astPescando.png',
    },
    {
        title: 'Navega por las Constelaciones de Tu Ser',
        description: '¿Eres un intrépido Leo lleno de pasión o un intuitivo Piscis conectado con lo místico? Conoce las estrellas que te acompañan desde el momento en que llegaste a este mundo. Sumérgete en las constelaciones de tu ser y entiende cómo cada alineación planetaria ha formado la maravillosa obra maestra que eres.',
        astro: '/img/astMontanod.png',
    },
    {
        title: 'Consejos Cósmicos para una Vida Brillante',
        description: 'Tu carta astral no solo revela quién eres, sino también cómo puedes vivir una vida más plena y satisfactoria. Descubre consejos cósmicos para maximizar tu potencial, mejorar tus relaciones y tomar decisiones acertadas alineadas con tu verdadera naturaleza estelar.',
        astro: '/img/astMeditando.png',
    },
    {
        title: 'No Dejes que el Universo Guarde Secretos',
        description: '¿Estás listo para embarcarte en un viaje fascinante hacia tu propia galaxia interior? ¡Conoce tu carta de nacimiento y despierta el poder de las estrellas en tu vida! El cosmos tiene un mensaje para ti, ¿estás listo para escucharlo? ¡Sumérgete en el fascinante mundo de tu carta astral y comienza a vivir la vida bajo la guía de las estrellas! ¡Tu destino te espera! ✨',
        astro: '/img/astCompartiendo.png',
    },
    ];
</script>

<style scoped>
    .v-carousel-item {
        background-color: transparent !important;
        padding-left: 5.5rem;
    }
    h2{
        color: beige;
        font-size: 3rem;
        font-weight: 1000;
    }
    p{
        color: azure;
    }
    .text-col{
        margin-top: 2rem;
    }
    .imageCarousel {
        margin-top: 4rem;
        margin-left: 6.35rem;
    }
</style>
