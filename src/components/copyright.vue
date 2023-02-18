<template>
	<footer>
		<div>Copyright 2023-Now kobe-koto</div>
		<br>
		<span>Under AGPL-3.0</span>
		<span>
			Powered by
			<a href="https://astro.build/">Astro</a>
			&
			<a href="https://vuejs.org/">Vue 3</a>
		</span>
		<span>
			Open Source on
			<a href="https://github.com/kobe-koto/Primula/">Github</a>
		</span>
	</footer>
</template>

<style scoped>
footer {
	text-align: center;
	padding: 45px 0;
	background-color: #16160e /*暗黒色 あんこくしょく*/ ;
}
footer > span:not(:last-child) {
	border-right-style: solid;
	border-right-color: #808080;
	border-right-width: 3px;
	padding-right: 5px;
	margin-right: 5px;
}
</style>