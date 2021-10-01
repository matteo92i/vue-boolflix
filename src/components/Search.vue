<template>
    <div></div>
</template>

<script>
import axios from "axios";

export default {
    name: "Search",

    data: function(){
        return{

        }
    },

    created: function (){
        axios.get("https://api.themoviedb.org/3/movie/550?api_key=b44f67a7438dbc78b01da40ce05c127a")
    }
    

    
}
</script>

<style>

</style>