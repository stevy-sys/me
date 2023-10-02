<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span>My</span>
          <span class="green--text">Services</span>
        </h2>
      </v-flex>
      <v-flex v-for="service in services" :key="service.src" xs6 sm3 md3 lg3 xl3>
        <v-card hover flat color="transparent" :style="{ 'cursor': 'context-menu' }">
          <v-card-title></v-card-title>
          <v-img :src="service.src" height="100" aspect-ratio="2.75" :alt="'Eldin do ' + service.title"
            lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif" contain></v-img>
          <v-card-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>{{ service.title }}</v-flex>
            <div>{{ service.description }}</div>
          </v-card-title>
        </v-card>
      </v-flex>
      <!-- <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span>My</span>
          <span class="green--text">Clients</span>
        </h2>
      </v-flex> -->

      <!-- <v-flex v-for="client in clients" :key="client.src" xs6 sm4 md3 lg2 xl2>
        <v-card flat :href="client.href" target="_blank" color="transparent">
          <v-hover>
            <v-img slot-scope="{ hover }" :src="client.src" :alt="client.name + ' logo'"
              lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif" height="100"
              width="160" aspect-ratio="2.75" contain>
              <v-expand-transition>
                <div v-if="!hover" class="transition-fast-in-fast-out green v-img--reveal" style="height: 100%;"></div>
              </v-expand-transition>
            </v-img>
          </v-hover>
        </v-card>
      </v-flex> -->
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: "Services",
    titleTemplate: "%s ← Stevy dev",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Eldin Zaimovic's Services Web Development Video Editing Graphic Design Front-End Advetising"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Stevy dev" },
      { property: "og:site_name", content: "Stevy dev" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://eldin.space" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg"
      },
      {
        property: "og:description",
        content:
          "Eldin Zaimovic's Services Web Development Video Editing Graphic Design Front-End Advetising"
      }
    ]
  },
  data() {
    return {
      clients: [
        {
          name: "Brandly",
          src: "https://i.imgur.com/BLJ16wb.png",
          href: "https://www.brandly.com/"
        },
        {
          name: "EEVOY",
          src: "https://i.imgur.com/lIJePVb.png",
          href: "https://www.eevoy.com/"
        },
        {
          name: "Riders Share",
          src: "https://i.imgur.com/pgkY80b.png",
          href: "https://www.riders-share.com/"
        },
        {
          name: "Esthetician Connection",
          src:
            "https://estheticianconnection.com/wp-content/uploads/2019/01/EC-logo.png",
          href: "https://estheticianconnection.com/"
        },
        {
          name: "Goldentimepieces",
          src: "https://i.imgur.com/sEybxZ5.png",
          href: "https://goldentimepieces.com/"
        },
        {
          name: "MFS-EMMAUS",
          src: "https://i.imgur.com/33xPmQ8.png",
          href: "https://mfs-emmaus.ba/"
        },
        {
          name: "Scanlister",
          src: "https://i.imgur.com/5K7h7c4.png",
          href: "https://www.scanlister.com/"
        },
        {
          name: "Unbroken Designs",
          src: "https://i.imgur.com/kDLRh64.png",
          href: "https://www.unbrokendesigns.com/"
        },
        {
          name: "VilaShirts",
          src: "https://i.imgur.com/Fg26T32.png",
          href: "https://www.instagram.com/_vilashirts_/"
        }
      ],

      services: [
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRz2vGkCemeOyt9T6_VOuN30VRrRchSruhuCw&usqp=CAU",
          title: "CRUD Front",
          description: "Création d'une interface utilisateur conviviale pour gérer vos données, y compris les opérations CRUD (Création, Lecture, Mise à jour, Suppression)."
        },
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTiboGHnKmaMXDG_c5_35bF-OnzMNg3n_pLwg&usqp=CAU",
          title: "CRUD Back",
          description: "Mise en place d'un backend robuste et sécurisé pour prendre en charge les opérations CRUD, assurant la fiabilité et la sécurité de votre application."
        },
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ3kXP6A5LTi5vqRoquahYqQ4ydeNN4EETCSg&usqp=CAU",
          title: "Websocket ou Socket.io",
          description: "Intégration de WebSockets ou Socket.io pour permettre des communications en temps réel, améliorant ainsi l'interaction entre les utilisateurs."
        },
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRdUUC8kMBurknY0KmQ_W0P95jKUk1OhNHk_A&usqp=CAU",
          title: "Système de Paiement",
          description: "Création d'un système de paiement sécurisé permettant aux utilisateurs d'effectuer des transactions en toute confiance sur votre plateforme."
        },
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRMUYIu1sVBKzzavRDZSP3wDia3CsXdE4JrMA&usqp=CAU",
          title: "Utilisation API Externe",
          description: "Intégration d'API externes pour enrichir votre application avec des fonctionnalités supplémentaires, améliorant ainsi l'expérience utilisateur."
        },
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ118AU1Mg-Zfmk53wcNFW4HWZt2ufdwrWA1Q&usqp=CAU",
          title: "Tests Unitaires",
          description: "Mise en place de tests unitaires pour garantir la stabilité de votre application et détecter les erreurs potentielles tôt dans le processus de développement."
        },
        {
          src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4IoofCPJUbEea5ymDTiXJmvgmnkC8-aVjeg&usqp=CAU",
          title: "Principe SOLIDE",
          description: "Application des principes SOLID (Single Responsibility, Open-Closed, Liskov Substitution, Interface Segregation, Dependency Inversion) pour créer un code propre, maintenable et extensible."
        }
      ]
    };
  }
};
</script>
<style >
.v-img--reveal {
  opacity: 0.3;
}
</style>