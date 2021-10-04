<template>
    <div class="flex">
        <div>
            <input type="text" placeholder="cerca il tuo film preferito" v-model= "needle">
        </div>
        <div>
            <button class="custom-botton" @click="$emit('ricerca', needle)">Cerca Film</button>
        </div>
    </div>
</template>

<script>


export default {
    name: "Search",

    data: function(){
        return{
            needle: '',
        }
    },



    


    

    
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