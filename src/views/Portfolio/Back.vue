<template>
    <v-container grid-list-xl>
      <h2 class="pl-4">
        <span>Web</span>
        <span class="green--text">Portfolio</span>
      </h2>
      <v-layout row justify-center align-center wrap class="mt-4 pt-2">
        <v-dialog
          v-model="project.dialog"
          lazy
          max-width="1000"
          v-for="project in projects"
          :key="project.title"
        >
          <template v-slot:activator="{ on }">
            <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
              <v-card hover flat color="transparent">
                <v-img
                  :src="project.poster"
                  :alt="project.title"
                  height="230"
                  lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
                ></v-img>
                <v-card-title primary-title class="justify-center">{{project.title}}</v-card-title>
              </v-card>
            </v-flex>
          </template>
          <v-card v-if="project.dialog">
            <v-img :src="project.poster"></v-img>
            <v-card-text>
              <h3 class="headline mb-0">
                <span>Technology</span>
              </h3>
              <v-chip color="green" v-for="techno in project.tech" text-color="white">{{techno}}</v-chip>
            </v-card-text>
            <v-card-text>
              <h3 class="headline mb-0">
                <span>Description</span>
              </h3>
              <div  v-for="description in project.description" text-color="white">{{description}}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn flat large dark color="green" :href="project.git" target="_blank">
                <v-icon left>fab fa-github</v-icon>GitHub
              </v-btn>
              <v-btn large flat dark color="green" :href="project.demo" target="_blank">
                <v-icon left>fas fa-desktop</v-icon>Demo
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-layout>
    </v-container>
  </template>
  
  <script>
  export default {
    metaInfo: {
      title: "Back Portfolio",
      titleTemplate: "%s ← Stevy dev",
      meta: [
        { name: "viewport", content: "width=device-width, initial-scale=1" },
        {
          name: "description",
          content:
            "Eldin Zaimovic's Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
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
            "Eldin Zaimovic's Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
        }
      ]
    },
    data() {
      return {
        dialog: false,
        projects: [
           {
            dialog: false,
            title: "API Sneat",
            git: "https://github.com/stevy-sys/Sneat.git",
            demo: "https://sneat.rubycorp.fr/api/documentation",
            tech: [
              "PHP",
              "Laravel",
              "Passport Token",
              "Swagger"
            ],
            poster: "/port/sneatapi.JPG",
            description:[
                "API reseau socio ",
                "amis / actualite / commentaire / reaction / profile / groupe"
            ]
          },
          {
            dialog: false,
            title: "API Lugx_gaming",
            git: "https://github.com/stevy-sys/lugx_gaming.git",
            demo: "https://lugx.rubycorp.fr/api/documentation",
            tech: [
              "PHP",
              "Laravel"
            ],
            poster: "/port/lugx.JPG",
            description:[
                "API e-commerce Gaming ",
                "produit / cart / panier / payment"
            ]
          },
          {
            dialog: false,
            title: "API Chat",
            git: "https://github.com/stevy-sys/chat-api.git",
            demo: "https://chat.rubycorp.fr/documentation",
            tech: [
              "PHP",
              "Laravel",
              "Sanctum token",
              "Websocket",
              "Swagger"
            ],
            poster: "/port/chatapi.JPG",
            description:[
                "API Chat message user ",
                "conversation groupe / conversation prive / message / presence en ligne / temp reelle"
            ]
          },
          {
            dialog: false,
            title: "Noah Voyage API",
            git: "",
            demo: "https://noah-voyages.com/",
            tech: [
              "PHP",
              "Laravel",
              "Passport",
              "Websocket",
              "Jquery"
            ],
            poster: "/port/noah.JPG",
            description:[
                "API Agence de voyage ",
                "circuit / customisation / reservation / paiment / "
            ]
          },
          {
            dialog: false,
            title: "StarterKit Stevy/Framwork",
            git: "https://github.com/stevy-sys/mon-framework.git",
            demo: "https://github.com/stevy-sys/mon-framework.git",
            tech: [
              "PHP",
              "symfony Console"
            ],
            poster: "",
            description:[
                "Back end inspirer de laravel",
                "Controller / Model / Migration / Vue / Commande console"
            ]
          },
          {
            dialog: false,
            title: "Stevy/Framwork",
            git: "https://github.com/stevy-sys/core.git",
            demo: "https://github.com/stevy-sys/core.git",
            tech: [
              "PHP",
              "Packagist"
            ],
            poster: "",
            description:[
                "Librairie package de PHP ",
                "Controller / Model / Migration / Vue / Commande console / Packagiste / composer"
            ]
          },
          
          {
            dialog: false,
            title: "RubyCorp",
            git: "https://github.com/stevy-sys/only-fan.git",
            demo: "https://rubycorp.fr/",
            tech: [
              "PHP",
              "Laravel",
              "Jquery",
              "VueJS"
            ],
            poster: "/port/rubycorp.JPG",
            description:[
                "Site de rencontre / onlyfan ",
                "Back office / gallerie / paiment / chat"
            ]
          },
          {
            dialog: false,
            title: "Chat API MERN",
            git: "https://github.com/stevy-sys/chat-node.git",
            demo: "https://eldin.space/",
            tech: [
              "NodeJS",
              "MongoDB",
              "Express",
            ],
            poster: "/port/chatapi.JPG",
            description:[
                "API Chat message user ",
                "conversation groupe / conversation prive / message / presence en ligne / temp reelle"
            ]
          }
        ]
      };
    }
  };
  </script>
  
  <style  scoped>
  </style>