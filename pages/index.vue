<template>
  <v-container fluid grid-list-md>
    <v-layout row wrap>
      <v-flex v-for="item in items" :key="item.id" xs12 md6 lg3>
          <v-card
            class="mx-auto"
            max-width="400"
          >
          <v-img
            class="white--text align-end"
            height="200px"
            :src="item.image"
          >
          </v-img>
          <v-card-title v-text="item.name"></v-card-title>
          <v-card-text class="text--primary">
            <p v-text="item.description"></p>
          </v-card-text>

          <v-card-actions>
            <v-btn
              color="orange"
              text
              :href="item.link"
		        	target="_blank"
            >
              Visit
            </v-btn>

            <v-btn
              color="orange"
              text
              :href="item.repository_link"
		        	target="_blank"
            >
              Repository
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  data () {
    return {
      items: [
        {
          id: 0,
          name: "About Me Website",
          description: "This is a very simple static website for my dicoding submission in Belajar Dasar Pemrograman Web class from Dicoding Academy.",
          link: "https://natanhp.github.io/About-Me-Website/index.html",
          repository_link: "https://github.com/natanhp/About-Me-Website",
          image: "about-me-website.png"
        },
        {
          id: 1,
          name: "Kouve Petshop Android Application Javadoc",
          description: "Auto-generated Javadoc of Kouvee Petshop Android Application.",
          link: "https://natanhp.github.io/Kouve-Petshop-Android-Doc",
          repository_link: "https://github.com/natanhp/Kouvee-Petshop-Android",
          image: "kouvee-petshop-android-doc.png"
        },
        {
          id: 2,
          name: "Kouvee Petshop Frontend",
          description: "This is the frontend version of Pengembangan Projek Perangkat Lunak's final submission.",
          link: "https://natanhp.github.io/Kouvee-Petshop-Frontend",
          repository_link: "https://github.com/natanhp/Kouvee-Petshop-Web-Frond-End",
          image: "kouvee-petshop-frontend.png"
        },
        {
          id: 3,
          name: "Kouvee Petshop Desktop Javadoc",
          description: "Auto-generated Javadoc of Kouvee Petshop Desktop Application.",
          link: "https://natanhp.github.io/Kouvee-Petshop-Desktop-Doc/",
          repository_link: "https://github.com/natanhp/Kouvee-Petshop-Desktop",
          image: "kouvee-petshop-dekstop-doc.png"
        },
      ],
    }
  },
}
</script>