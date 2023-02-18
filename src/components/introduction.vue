<template>
    <div class="IntroductionContainer">
        <div class="Introduction">
            <h2>{{ Title }}</h2>
            <p>{{ Description }}</p>
			<a class="as-button bg-transparent" :href="Href" v-if="Href">
				<span>
					Getting Started &nbsp;
					<i class="fa-solid fa-arrow-right"></i>
				</span>
			</a>
        </div>
    </div>
</template>


<style scoped>
    div.IntroductionContainer {
        /* size */
        min-height: 400px;
		padding-top: 55px;
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

       	-webkit-align-items: center;
		-webkit-box-align: center;
		align-items: center;

		-webkit-justify-content: center;
		-webkit-box-pack: center;
		justify-content: center;

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

<script setup>
const { Title, Description, Href } =
	defineProps({
		Title: {
			type: String,
			required: true
		},
		Description: {
			type: String,
			required: true
		},
		Href: {
			type: String,
			required: false
		}
	});
function Go (Href) {
	location.assign(Href)
}
</script>
