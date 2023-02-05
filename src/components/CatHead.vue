<template>
	<div class="head">
		<div class="ear ear--left"></div>
		<div class="ear ear--right"></div>
		<div class="nose-up"></div>
		<div class="nose-down"></div>
		<div class="mouth"></div>
		<div class="eye eye--left"></div>
		<div class="eye eye--right"></div>
		<div class="eye eye--inside"></div>
		<div class="mustache mustache--left"></div>
		<div class="mustache mustache--right"></div>
	</div>
</template>

<style>
.head {
	background-color: rgb(35, 35, 35);
	height: 150px;
	width: 150px;
	border-radius: 90px 90px 70px 70px;
	position: absolute;
	bottom: 260px;
	right: 200px;
}

.ear {
	height: 60px;
	width: 40px;
	background-color: rgb(35, 35, 35);
	position: absolute;
	bottom: 115px;
}

.ear--left {
	left: -1%;
	border-radius: 70% 30% 0% 0% / 100% 100% 0% 0%;
	transform: rotate(-20deg);
}

.ear--right {
	right: -1%;
	border-radius: 30% 70% 0% 0% / 100% 100% 0% 0%;
	transform: rotate(20deg);
}

.nose-up {
	height: 20px;
	width: 30px;
	background-color: rgb(119, 42, 61);
	position: absolute;
	bottom: 50px;
	right: 55px;
	border-radius: 50% 50% 50% 50% / 30% 30% 70% 70%;
}

.nose-down {
	height: 30px;
	width: 30px;
	background-color: rgb(65, 65, 65);
	position: absolute;
	bottom: 30px;
	right: 65px;
	box-shadow: 20px 0 rgb(65, 65, 65);
	border-radius: 50%;
}

.mouth {
	height: 15px;
	width: 20px;
	background-color: rgb(207, 2, 2);
	position: absolute;
	bottom: 20px;
	right: 60px;
	border-radius: 50% 50% 50% 50% / 30% 30% 70% 70%;
}

.eye {
	height: 40px;
	width: 40px;
	background-color: rgb(248, 248, 248);
	position: absolute;
	bottom: 75px;
	animation: eye-blink 2s infinite 3.5s;
}

.eye--left {
	left: 28px;
	border-radius: 70% 30% 0% 0% / 100% 100% 0% 0%;
}

.eye--right {
	right: 24px;
	border-radius: 30% 70% 0% 0% / 100% 100% 0% 0%;
}

.eye--inside {
	height: 30px;
	width: 30px;
	background-color: rgb(0, 0, 0);
	position: absolute;
	bottom: 75px;
	right: 88px;
	border-radius: 50%;
	box-shadow: 60px 0 rgb(0, 0, 0);
}

@keyframes eye-blink {
	0% {
		transform: scaleY(1);
	}

	18% {
		transform: scaleY(1);
	}

	20% {
		transform: scaleY(0);
	}

	38% {
		transform: scaleY(1);
	}

	45% {
		transform: scaleY(1);
	}

	80% {
		transform: scaleY(1);
	}
}

.mustache {
	height: 2px;
	width: 35px;
	position: absolute;
	background-color: rgb(0, 0, 0);
	box-shadow: 0 10px rgb(0, 0, 0), 0 20px rgb(0, 0, 0);
}

.mustache--left {
	bottom: 55px;
	right: 85px;
	transform: rotate(10deg);
}

.mustache--right {
	bottom: 55px;
	right: 20px;
	transform: rotate(-10deg);
}
</style>
