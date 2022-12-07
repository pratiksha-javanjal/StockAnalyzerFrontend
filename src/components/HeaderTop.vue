<template>
    <div id="top">
        <h1> {{bookName}} </h1>
        <!-- <h4> {{authorName}} </h4> -->
    </div>
</template>
    
    <script>
    
    export default{
        name: 'HeaderTop',
        props:{
            bookName: String
            
        }
    }
    
    </script>
    
    <style scoped>
    
    #top{
        padding: 10px;
        background-color: #0a1612;;
        text-align: center;
        grid-area: top;
        max-width: 100%;
        border-radius: 5px;
        color: beige;
    }
    #top h1{
        padding-top: 30px;
        font-size: 3em;
    }
    
    </style>