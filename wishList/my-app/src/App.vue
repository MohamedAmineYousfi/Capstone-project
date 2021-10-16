<template>
  <v-app   max-width ="70%">
    <v-main >

      RELATED PRODUCTS
      <HorizontalListRelated></HorizontalListRelated>
       YOUR OUTFIT
      <HorizontalListYourOutfit></HorizontalListYourOutfit>
      
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
    // RelatedProduct: RelatedProduct,
    // WishProduct : WishProduct,
    // BtnFav : BtnFav,
    HorizontalListRelated :HorizontalListRelated,
    HorizontalListYourOutfit : HorizontalListYourOutfit 

  },

  data: () => ({
    alignments: ["start"],
    list: {
      // 1200 because @media (min-width: 1200px) and therefore I want to switch to windowed mode
      windowed: 1200,

      // Because: #app {padding: 80px 24px;}
      padding: 24,
    },
    items: [{ title: "Item 0", content: "Content item with description" }],
  }),
};
</script>
