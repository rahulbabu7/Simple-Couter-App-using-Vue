<script setup>
import {ref} from 'vue'
let count = ref(0)

/*

NOT THE EASY WAY TO INCREASE THE COUNT


const addCount = ()=>{
count.value = count.value +1
}
const subCount = ()=>{
count.value = count.value - 1
}

*/

console.log(count)
</script>

<template>
<main>
    <section>
        <h4>
            The current count is... 
        </h4>
        <div class="count">
            <h2>
            {{ count }}
        </h2>
        </div>
     <!-- Simplest way of incrementing count -->
        <button @click="count++">+</button>
        <button @click="count--">-</button>

        <!-- not the simplest -->
        <!-- <button @click="addCount">+</button>
        <button @click="subCount">-</button> -->
    </section>
</main>

</template>

<style scoped>
main{
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center; /*Horizontally center */
    align-items: center;
}
h4{
    font-size:xx-large;
    font-weight: 900;
}
.count{
    display:flex ;
    justify-content: center;
}
button{
    padding: 10px 30px;
    margin-left: 30px;
    margin-top: 20px;
}

</style>