<template>
  <v-app   max-width ="70%">
    <v-main >
<v-container class="ma-16"> 
      RELATED PRODUCTS
      <HorizontalListRelated></HorizontalListRelated>
       YOUR OUTFIT
      <HorizontalListYourOutfit></HorizontalListYourOutfit>
</v-container>
    </v-main>
  </v-app>
</template>

<script>
// import BtnFav from "./components/BtnFav.vue"
import HorizontalListYourOutfit from "./components/HorizontalListYourOutfit.vue"
import HorizontalListRelated from "./components/HorizontalListRelated.vue"


export default {
  name: "App",

  components: {
    HorizontalListRelated :HorizontalListRelated,
    HorizontalListYourOutfit : HorizontalListYourOutfit 
  },

  data: () => ({
    alignments: ["start"],
    list: {
      // 1200 because @media (min-width: 1200px) and therefore I want to switch to windowed mode
      windowed: 1200,

      // Because: #app {padding: 80px 24px;}
      padding: 15,
    },
    items: [{ title: "Item 0", content: "Content item with description", margin : 0 },],
  }),
};
</script>
