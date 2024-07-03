<script setup>
import api from "../services/api"
import {useDictionaryStore} from "../stores/WordStore.js"

    var WordStore = useDictionaryStore();


    const GetWord = (word) => {
        api.get(`${word}`).then((response) => {
            var data = response.data 
            console.log(data)
        })
    }

</script>

<template>
    <main>
        <main class="main-content">
            <h2>{{WordStore.word}}</h2>
        </main>
        
    </main>
</template>

<style scoped>

</style>
