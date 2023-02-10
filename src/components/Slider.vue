<template>
    <div class="SliderContainer">
	    <div>
		    <img src="/images/2022-02-19-20-38-44_1080_commpressed.png" alt="" />
    	</div>
    	<div>
		    <img src="/images/2022-02-19-20-49-05_1080_commpressed.png" alt="" />
	    </div>
    	<div>
	    	<img src="/images/2022-02-20-15-40-05_1080_commpressed.png" alt="" />
    	</div>
    	<div>
	    	<img src="/images/herobg.png" alt="" />
    	</div>
    </div>
</template>
<!--   
<script setup>

</script> -->

<style scoped>
.SliderContainer {
    width: 100%;
    margin: 30px auto;
    height: 400px;
    background-color: #1f1f1f;
}
.SliderContainer div.placeholder {
    width: 100%;
    position: absolute;
}
.SliderContainer div.placeholder img {
    width: 100%;
}
.SliderContainer div:not(.placeholder) {
    opacity: 0;
    animation: round 20s linear infinite;
    /* position: absolute; */
}
.SliderContainer div:not(.placeholder) img {
    width: 100%;
    position: absolute;
}


.SliderContainer div:not(.placeholder):nth-child(1) {
    animation-delay: .5s;
}

.SliderContainer div:not(.placeholder):nth-child(2) {
    animation-delay: 4.5s;
}

.SliderContainer div:not(.placeholder):nth-child(3) {
    animation-delay: 9s;
}

.SliderContainer div:not(.placeholder):nth-child(4) {
    animation-delay: 13.5s;
}




@keyframes round {
    0%, 25% {
        opacity: 0;
    }
    2.5%, 22.5% {
        opacity: 1;
    }
}

</style>
