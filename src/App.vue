<script>
import TopList from './components/TopList.vue'

let pairsObject = {}

// add Access-Control-Allow-Origin: *


export default {
  name: 'app',
  components: {
    TopList
  },
  data() {
    return {
      pairs: {}
    };
  },
  mounted() {
    fetch('/api/exchange/markets/tickers/all', {
      method: 'GET',
      headers: {
        'Content-Type': 'application/json',
        'Access-Control-Allow-Origin': '*'
      }
    })
      .then(response => response.json())
      .then(data => {

        this.pairs = Object.values(data.data.result)

        this.pairs = this.pairs.map(pair => ({
          ...pair,
          percentage: Math.random() * 10
        }));

        this.pairs.sort((a, b) => b.percentage - a.percentage);
        this.pairs = this.pairs.slice(0, 10);
      })
  }
}

</script>

<template>
  <TopList v-bind:pairs="pairs">

  </TopList>
</template>
