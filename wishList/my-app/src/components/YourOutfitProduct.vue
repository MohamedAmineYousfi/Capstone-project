<template >


<v-card  
    
    class="mx-auto my-12"
    max-width="374"
  >
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img
      height="400"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    ></v-img>
    <div class="my-4 text-subtitle-1">
       CATEGORY
      </div>
    <v-card-title>Expanded Product Name</v-card-title>

  

      <div class="my-4 text-subtitle-1">
        $ 123
      </div>

      <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
    

  <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
  
        <v-rating
          v-model="rating"
          color="yellow darken-3"
          background-color="grey darken-1"
          empty-icon="$ratingFull"
          half-increments
          hover
          large
        ></v-rating>
        </v-row>
      </v-card-text>


    <v-card-actions>
    
    </v-card-actions>
  </v-card>
</template>

<script>
  export default {
    name: 'YourOutfitProduct',

    data: () => ({

    }),
  }
</script>
