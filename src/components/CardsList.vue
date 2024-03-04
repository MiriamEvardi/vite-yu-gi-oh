<script>
import CardItem from './CardItem.vue';

import {store} from '../data/store.js';

export default {
  name: 'CardsList',
 
      components: {
        CardItem,
      },
    
      data() {
        return {
          store,
      }
    }
}
</script>

<template>
  <div class="container">
    <ul>
    
      <CardItem v-for=" currentCard in store.cards" :card="currentCard">

      </CardItem>
    </ul>
  </div>
</template>

<style lang="scss">
ul {
    list-style-type: none;

   display: flex;
   flex-flow: row wrap;
    
    
}
</style>
