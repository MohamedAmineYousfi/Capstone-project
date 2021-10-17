<template >
<vue-horizontal-list
  :items="items"
  :options="{
    responsive: [
      { end: 300, size: 1 },
      { start: 150, end: 300, size: 2 },
      { size: 4 },
    ],
  }"
>


  <template v-slot:default="{item}">
    <div class="item grid-list-md">
      <h5>{{item.title}}</h5>
<v-card  
    height="300"
    class="mx-200 my-2"
    max-width="180"
  >
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="5"
        indeterminate
      ></v-progress-linear>
    </template>
    <v-img
      height="190"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    >
    <button class="btn btn-sm btn-primary img-overlay ml-16 pl-16" v-on:click="togglefav" >
 <v-icon right>mdi-delete</v-icon>
      <i v-bind:class="['is_fav' ?  'fa-star' : 'fa-star-o', 'fa']" aria-hidden="true">
        </i></button>        
    </v-img>
    <div class=" text-subtitle-1">
       CATEGORY
      </div>
    <v-card-title  class=" text-subtitle-2">Expanded Product Name</v-card-title>
      <div class=" text-subtitle-0 ">
        $ 123
      </div>
  <v-card-text>
      <v-row
        align="center"
        class="xs-0"
      >
        <v-rating
          v-model="rating"
          color="yellow darken-3"
          background-color="grey darken-1"
          empty-icon="$ratingFull"
          half-increments
          hover
          x-small
        ></v-rating>
        </v-row>
      </v-card-text>


    <v-card-actions>
    
    </v-card-actions>
  </v-card>



    </div>
  </template>
</vue-horizontal-list>




</template>

<script>
import VueHorizontalList from "vue-horizontal-list";


  export default {
    name: 'HorizontalList',
    components: {
    VueHorizontalList,
  },
      props:['is_fav'],
    methods:{
      togglefav:function(){
        this.$emit('togglefav',!this.is_fav);
      }
    },

    data: () => ({
items: [{ title: "", content: "Content item with description", margin : 20 },{ title: "", content: "Content item with description", margin : 0 },{ title: "", content: "Content item with description", margin : 0 },{ title: "", content: "Content item with description", margin : 0 },{ title: "", content: "Content item with description", margin : 0 },{ title: "", content: "Content item with description", margin : 0 },],
    }),
  }
</script>
