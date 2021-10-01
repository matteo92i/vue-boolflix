<template>
    <div class="flex">
        <div>
            <input type="text" placeholder="cerca il tuo film preferito">
        </div>
        <div>
            <button class="custom-botton">Cerca Film</button>
        </div>
    </div>
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
        .then((film) => {
            console.log(film)

        })
    }
    

    
}
</script>

<style>
input{
    width: 200px;
}
    
    
.flex{
    display: flex;
    justify-content: center;
}
.custom-botton{
    
    background-color: red;
    font-size: 15px;
}

</style>