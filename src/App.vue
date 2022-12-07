<template>
  <div class="container">
    <HeaderTop bookName="STOCK ANALYZER" />

    <StockMain :stocks="stocks" />

    <div class="footer">
      <p>PRATIKSHA JAVANJAL</p>
    </div>

</div>
</template>

<script>

import HeaderTop from './components/HeaderTop.vue'
import StockMain from './components/StockMain.vue'

export default {
  name: 'App',
  components: {    
    HeaderTop,
    StockMain
  },

  data(){
    return {
      stocks: []
    }

  },

  methods: {

    // promises

      async fetchStocks(){
          const response = await fetch('https://gray-brave-dragonfly.cyclic.app/api')
          const data = await response.json()
          console.log( data )
          return data
      }


  },
  async created(){
    this.stocks = await this.fetchStocks()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: #c5c1c0;
}
.container {
  max-width: 1400px;
  margin: 10px auto;
  overflow: auto;
  min-height: 300px;
  /* border: 0.1em solid black; */
  padding: 30px;
  border-radius: 15px;
  display: grid;
  grid-template-rows: 0.07fr 5fr 0.5fr 0.1fr ;
  grid-template-columns: 0.5fr 1fr;
  grid-template-areas: 
  "top top"
  "headInfo headInfo"
  "cDetail1 cDetail2 "
  "eDetails eDetails"
  ;
}

div{
  margin-bottom: 0.3em;
}

</style>
