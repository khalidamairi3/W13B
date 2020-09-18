<template>
    <div id="tweet">
        <h1> {{ user }}</h1>
        <h6> {{date}} </h6>
        <h4 > {{ content}}</h4>
        <h2 @click="like = true" v-if="!like"> Like</h2>
        <h2 @click="like = false" v-else> unlike</h2>


    </div>
    
</template>

<script>
export default {
    name: "page-tweet",
    props:{
        user :{
         type:String,
         required: true,
         default: "user",
         
        },
        content:String,
        date:String,

    },
    data: function(){
        return{
            like : false,

        }

    }
}

</script>

<style  scoped>

#tweet{
    width: 50%;
    border: 1px solid black;
    border-radius: 15px 15px 15px 15px; 
    
}
</style>