<script setup>
import { ref } from 'vue';



const props = defineProps({
    img:{
        type: String
    },
    alt:{
        type:String
    },
    class:{
        type: String
    },
    text:{
        type: String
    }
})



</script>



<template>

    <div :class="class">
        <img :src="'src/img/' + props.img" :alt="alt">
        <p>{{props.text}}</p>
        
    </div>
    

</template>


<style scoped>


div{
    display: flex;
    flex-direction: column;
    max-width: 320px;
    padding: 10px;
    border-radius: 2%;
    background-color: #f0f0f0;
    box-shadow: 7px 5px 9px 0px rgba(0,0,0,0.29);
    margin: 10px;
}

img{
    max-width: 300px;
    max-height: 300px;
}

</style>