<template>
    <div class="IntroductionContainer">
        <div class="Introduction">
            <h2>Primula Introduction</h2>
            <p>這是什麼? 這是一個什麼都沒寫的網站前端.</p>
            <button class="bg-transparent">
                <a>
                    Getting Started &nbsp;
                    <i class="fa-solid fa-arrow-right"></i>
                </a>
            </button>
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
        background-attachment: fixed;
        background-image: url("/images/2022-02-20-15-40-05_1080_commpressed.png");

        /* item center */
        display: -webkit-box;
        display: -webkit-flex;
        display: flex;

        justify-content: center;
        align-items: center;
        
       	-webkit-align-items: center;
	-webkit-box-align: center;

	align-items: center;

	-webkit-justify-content: center;



    -webkit-box-pack: center;

	justify-content: center;
        
        padding-top: 55px;
    } 
    div.Introduction {
        text-align: center;
    }
    @media (max-width: 600px) {
        div.IntroductionContainer {
            padding-top: 80px;
        }
    }
</style>



<!-- <script setup></script> -->
