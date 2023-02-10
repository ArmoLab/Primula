<template>
    <div class="IntroductionContainer">
        <div class="Introduction">
            <h2>Introduction</h2>
            <button class="bg-transparent">Getting Started ></button>
        </div>
    </div>
</template>


<style scoped>
    div.IntroductionContainer {
        /* size */
        min-height: 400px;
        width: 100%;

        /* background */
        background-color: #1f1f1f;
        background-position: center;
        background-size: cover;
        background-image: url("/images/2022-02-20-15-40-05_1080_commpressed.png");

        /* item center */
        display: -webkit-box;
        display: -webkit-flex;
        display: flex;

        justify-content: center;
        align-items: center;
    } 
    div.Introduction {
        text-align: center;
    }
    button {
        border-style: solid;
        border-color: #f8f8ff;
        border-width: 2px;
        border-radius: 5px;

        padding: 15px 10px;

        color: #f8f8ff;
        font-size: medium;
        font-weight: bold;
    }
    button.bg-transparent {
        background-color: rgba(0,0,0,0);
    }
</style>



<!--   <script setup>
</script> -->