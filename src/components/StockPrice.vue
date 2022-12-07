<template>

    <div>
    <div class="main">
        <h2> {{stock.name}}</h2>
        <h4> <b>About -</b>  {{stock.about}}</h4>
    </div>
        <div class="currentDetails">
          
                <h4> Current Price : Rs {{stock.currentPrice}}</h4>

            
           
            <div class="right">
                <h4> Today's High : Rs {{stock.high}}</h4>
                <hr>
                <h4> Today's Low  : Rs {{stock.low}}</h4>
            </div>
            
        </div>
        
        <div class="extraDetails">
           <ul>
            <li>   MARKEPT CAP : Rs {{stock.marketCap}} Cr.</li>
            <li>   STOCK PE : {{stock.stockPE}} </li>
            <li>   STOCK ROCE : {{stock.roce}} </li>
           </ul>

        </div>
      
    </div>



</template>

<script>


export default{
    name: 'StockPrice',
    props:{
        stock: Array
    }
}


</script>

<style scoped>
.extraDetails  li{
    padding: 20px;
    font-size: 2em;;
    text-decoration: none;
    list-style: none;
}
.extraDetails {
    grid-area: eDetails;
    background-color: #1a2930;
    color:whitesmoke;
    /* padding: 20px; */

}

.right {
    grid-area: cDetail2;
    background-color: #C5c1c0;
    color: black;
    justify-content: flex-end;
}
.right h4 {
    font-size: 1.5rem !important; 
}

.currentDetails{
    grid-area: cDetail1;
    background-color:#1a2930;
    color: white;
    padding: 30px;
    display: flex;
    justify-content: space-around;
}
.currentDetails h4 {
    font-size: 3rem;
}

.main {
    background-color: #1a2930;
    padding: 20px;
    grid-area: headInfo;
    color: whitesmoke;
}
.main h2{
    font-size: 3.5rem;
    /* padding-top: 40px ; */
    /* color: #1a2930; */
}
.main h4{
    padding: 20px;
    font-size: 1rem;

}

h4{
    margin: 2px;
}

div{
 
    padding: 3em;
}

.red{
background-color: orangered !important;

}
.green{
    color: white;
}


</style>