<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Education</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item v-for="item in education " color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">{{item.date_end}} -</div>
                <div class="caption font-weight-bold green--text">{{item.date_start}}</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>{{item.title}}</strong>
                <div class="caption mb-2">{{item.description}}</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>


    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experience</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>

          <v-timeline-item  v-for="item in experience " color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">{{item.date_end}} -</div>
                <div class="caption font-weight-bold green--text">{{item.date_start}}</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>{{item.title}}</strong>
                <div class="caption mb-2"><strong>{{item.technologie}}</strong></div>
                <div class="caption mb-2">{{item.description}}</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Front</span>
          <span class="green--text">Skills</span>
        </h2>
        <br>
        <div v-for="item in technologie.front">
          <strong>{{item.title}}</strong>
          <v-progress-linear v-model="item.capacity" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        </div>
        
      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Back</span>
          <span class="green--text">Skills</span>
        </h2>
        <br>
        <div v-for="item in technologie.back">
          <strong>{{item.title}}</strong>
          <v-progress-linear v-model="item.capacity" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        </div>
        
      </v-flex>
      <!-- <div class="mt-4 pt-2">
        <v-btn
          href="https://docs.google.com/document/d/1WSR42FEgUahJuR_RArW1wz7TfUBlgj13zekRidmQgs4/edit?usp=sharing"
          target="_blank"
          color="green"
          dark
          large
        >
          Download Resume
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div> -->
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Resume",
    titleTemplate: "%s ← Stevy dev",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
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
          "Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
      }
    ]
  },
  data() {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0,
      education:[
        {
          date_start:"2020",
          date_end:"2021 ",
          title:"License II en informatique de Gestion  ",
          description:"CNTMAD"
        },
        {
          date_start:"2019",
          date_end:"2020 ",
          title:"License I en informatique de Gestion  ",
          description:"CNTMAD"
        },
        {
          date_start:"2016",
          date_end:" ",
          title:"Baccalauréat   ",
          description:"Lycée Filadelfia Antsirabe  Série D Mention Assez-Bien "
        }
      ],
      experience:[
        {
          date_start:"05/02/2023 ",
          date_end:"",
          title:" Développeur Front-End Télétravail",
          technologie:"VueJS ",
          description:" Application de rencontre rubycorp.fr "
        },
        {
          date_start:"21/09/2022 ",
          date_end:"20/12/2022 ",
          title:"Développeur Front-End SAYNA WORK",
          technologie:"Angular ",
          description:"Gomed API , Gomed Admin , Gomed Store, Gomed User "
        },
        {
          date_start:"20/09/21 ",
          date_end:"01/03/22 ",
          title:"Développeur Front-End MKWEBLINKNS ",
          technologie:" VueJS , NuxtJS , Angular ",
          description:"  Noah-Voyage, Zowanj, ShareMyHobbies,  Aba-world "
        },
        {
          date_start:" 14/12/2020",
          date_end:"06/03/2021 ",
          title:"Développeur PHP Télétravail Tic Toc Family ",
          technologie:"  Laravel PHP et Jquery ",
          description:"  Application web agence immobilier Bailti.fr"
        },
        {
          date_start:" 09/11/2020 ",
          date_end:"13/11/2020",
          title:"Hackathon organiser par IFM AFD et Orange ",
          technologie:" Symfony ,ReactJS  ",
          description:" Réalisation d’application dont le thème est la Biodiversité"
        },
        {
          date_start:" 23/02/2020 ",
          date_end:"23/03/2020  ",
          title:"Startup Soah Intégrateur web wordpress  ",
          technologie:" wordpress ",
          description:" Collaboration sur la réalisation du site web d’une  startup agro-business soah.mg"
        },
        {
          date_start:" 2019 ",
          date_end:"",
          title:"Projet personnel sur github",
          technologie:"react ",
          description:"calculatrice, jeux, mon portfolio, tableau de bord, application Skoto  ,... "
        },
      ],
      technologie:{
        front:[
          {
            title:"JavaScript",
            capacity:80
          },
          {
            title:"Jquery",
            capacity:80
          },
          {
            title:"VueJS",
            capacity:80
          },
          {
            title:"Angular",
            capacity:70
          },
          {
            title:"ReactJS",
            capacity:60
          },
        ],
        back:[
          {
            title:"PHP",
            capacity:80
          },
          {
            title:"Laravel",
            capacity:90
          },
          {
            title:"Symfony",
            capacity:75
          },
          {
            title:"NodeJS",
            capacity:75
          },
        ]
      }
    };
  },
  mounted() {
    this.startBuffer();
  },

  beforeDestroy() {
    clearInterval(this.interval);
  },

  methods: {
    startBuffer() {
      this.interval = setInterval(() => {
        this.buffer1 = 90;
        this.buffer2 = 85;
        this.buffer3 = 80;
        this.buffer4 = 80;
        this.buffer5 = 90;
        this.buffer6 = 70;
      }, 1000);
    }
  }
};
</script>
<style scoped>
</style>

