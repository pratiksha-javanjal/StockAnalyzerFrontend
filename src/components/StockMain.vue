<template>
    <div class="StockMain">


        

        <div v-for="stock in stocks" :key="stock.id" >
            <StockPrice :stock="stock"/>
        </div>

    </div>
    


</template>'

<script>

    import StockPrice from './StockPrice.vue'


    export default{
        name: 'StockMain',
        components: {
            StockPrice
        },
        props:{
            
            stocks: Array
        }
    }

</script>

<style scoped>

.StockMain{
grid-area: headInfo;

background-color: #c5c1c0;
padding: 1em;
color: gray;
}

</style>