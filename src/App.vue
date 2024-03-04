<script>
import axios from 'axios';
import { store } from './data/store';

export default {
  data() {
    return {
      cards: [],

      store,
    }
  },

  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then(res => {
      this.store.cards = res.data.results;
    }).catch(err => {
      console.log(err)
    })
  },

  components: {

  }
}

</script>

<template>
  
</template>

<style>

</style>
