<template>
	<div class="body">
		<div class="paw paw--left"></div>
		<div class="paw paw--right"></div>
		<div class="tail"></div>
		<div class="heart"></div>
	</div>
</template>

<style>
.body {
	background-color: rgb(35, 35, 35);
	height: 150px;
	width: 190px;
	border-radius: 90px 90px 70px 70px;
	position: absolute;
	bottom: 120px;
	right: 230px;
	border-radius: 110px 40px 40px 20px;
	animation: body-moving 2s infinite;
	transform-origin: bottom;
}

@keyframes body-moving {
	60% {
		transform: scale(0.9, 1.05);
	}
}

.paw {
	height: 40px;
	width: 40px;
	background-color: rgb(65, 65, 65);
	position: absolute;
	bottom: 1px;
}

.paw--left {
	left: 75px;
	border-radius: 70% 30% 0% 0% / 100% 100% 0% 0%;
	transform: rotate(105deg);
}

.paw--right {
	right: 24px;
	border-radius: 30% 70% 0% 0% / 100% 100% 0% 0%;
	transform: rotate(-100deg);
}

.tail {
	width: 75px;
	height: 140px;
	position: absolute;
	left: -60px;
	bottom: 20px;
	border-radius: 200px;
	box-shadow: inset 15px 20px 0px rgb(35, 35, 35);
	transform: rotate(235deg);
	animation: wave 3s infinite;
}

@keyframes wave {
	50% {
		transform-origin: 50px 50px;
	}
}

.heart {
	background-color: red;
	display: inline-block;
	height: 30px;
	width: 30px;
	left: 120px;
	bottom: -30px;
	position: relative;
	transform: rotate(-45deg);
	animation: heart 0.6s linear infinite;
}

@keyframes heart {
	0% {
		transform: rotate(-45deg) scale(1.1);
	}
	80% {
		transform: rotate(-45deg) scale(1);
	}
	100% {
		transform: rotate(-45deg) scale(0.7);
	}
}

.heart:before,
.heart:after {
	content: '';
	background-color: red;
	border-radius: 50%;
	height: 30px;
	position: absolute;
	width: 30px;
}

.heart:before {
	top: -15px;
	left: 0;
}

.heart:after {
	left: 15px;
	top: 0;
}
</style>
