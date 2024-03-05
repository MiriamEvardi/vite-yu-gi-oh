<script>
import CardItem from './CardItem.vue';
import AppCount from './AppCount.vue';

import {store} from '../data/store.js';

export default {
  name: 'CardsList',
 
      components: {
        CardItem,
        AppCount
      },
    
      data() {
        return {
          store,
      }
    },


}
</script>

<template>
  
  <div class="container">
   
      <AppCount></AppCount>
      <ul>
        <CardItem v-for=" currentCard in store.cards" 
        :card="currentCard">

        </CardItem>
      </ul>
    
  </div>
</template>

<style lang="scss">

@use '../style.scss' as *;

ul {
   list-style-type: none;

   display: flex;
   flex-flow: row wrap;
   gap: 20px;

   background-color: white;
   border: solid white 40px;
   border-top: 0;
    
  }
</style>
