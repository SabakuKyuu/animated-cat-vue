<template>
	<div class="ball"></div>
</template>

<style>
.ball {
	background-color: rgb(8, 11, 201);
	height: 50px;
	width: 50px;
	border-radius: 50%;
	position: relative;
	bottom: -130px;
	right: -130px;
	animation: bouncing 3s infinite;
}

@keyframes bouncing {
	10% {
		height: 50px;
		width: 50px;
	}
	30% {
		height: 50px;
		width: 40px;
	}
	50% {
		height: 30px;
		width: 55px;
		transform: translateY(240px);
	}
	75% {
		height: 50px;
		width: 55px;
	}
	100% {
		transform: translateY(0px);
	}
}
</style>
