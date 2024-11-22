
<script setup>
import { ref } from 'vue'


const name = "Pepito"
let counter = ref(5)

let characters = ref([])

function add(){
    counter++
    characters.value.push(counter.value)
}
function substrac(){
    counter--
    console.log(counter)
}

</script>

<template>
    <div class="bg-slate-300 max-w-96 rounded py-4 px-6 mx-auto text-center">Hola {{ name }}

    <div v-if="counter > 0" class="flex items-center justify-center rounded-full size-8 text-white bg-red-600">
        {{ counter }}
    </div>
    <div v-else">
        Nadie te escribe :(
    </div>

    <div @click="add" class="flex items-center justify-center rounded-full size-8 text-white bg-red-600">
        +
    </div>
    <div @click="substrac" class="flex items-center justify-center rounded-full size-8 text-white bg-red-600">
        -
    </div>
    </div>
    <div v-for="(name,index) in characters":key=index class="bg-green-500 mb-1">
{{ name }}
    </div>
</template>