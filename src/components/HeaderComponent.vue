<script setup>
    import {useDictionaryStore} from "../stores/WordStore.js"

    const WordStore = useDictionaryStore();

    function FindWord(word) {
        WordStore.word = word;d = word;
    }

</script>

<template>
    <header>
        <div class="header-content">
            <div class="search_content">
                <input type="text" @keyup="FindWord(word)" placeholder="Type a word" v-model="word">
                <button @click="FindWord(word)">
                    <i class="fa-sharp fa-solid fa-magnifying-glass"></i>
                </button>
            </div>
        </div>
    </header>
</template>

<style>
    header {
        background-color: #AAC4FF;
    }
    .header-content {
        max-width: 1200px;
        height: 80px;
        margin: 0 auto;
        padding: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .header-content .search_content {
        display: flex;
    }
    .header-content .search_content input {
        height: 40px;
        width: 400px;

        border: 2px solid #6d6d6d;
        margin: 1px;
        outline: none;
        padding: 10px;
        border-radius: .7em;

        font-weight: bold;
        text-align: center;
        color: #AAC4FF;

    }
    .header-content .search_content input::placeholder {
        color: #AAC4FF;

    }
    .header-content .search_content button {
        height: 40px;
        width: 40px;
        background-color: #ffff;

        border: 2px solid #6d6d6d;
        outline: none;
        border-radius: 50%;
        margin-left: 10px;

        cursor: pointer;

        display: flex;
        justify-content: center;
        align-items: center;
    }
    .header-content .search_content button i {
        color: #AAC4FF;
        font-size: 1.4em;
    }
</style>
