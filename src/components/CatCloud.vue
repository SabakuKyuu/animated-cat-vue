<template>
	<div class="cloud">
		<h3 class="title">
			<p class="cloud-word cloud-word-1" style="text-align: center"><strong>i really </strong></p>
			<p class="cloud-word cloud-word-2" style="text-align: center"><strong>need </strong></p>
			<p class="cloud-word cloud-word-3" style="text-align: center"><strong>this job!</strong></p>
		</h3>
	</div>
</template>

<style>
.cloud {
	background-color: rgb(255, 255, 255);
	height: 150px;
	width: 150px;
	border-radius: 50px 50px 50px 5px;
	position: absolute;
	bottom: 350px;
	right: 30px;
	text-align: center;
	animation: cloud-move 2s infinite;
}

@keyframes cloud-move {
	50% {
		transform: scale(1.2);
	}
}

.cloud-word {
	animation: color-animation 4s linear infinite;
}

.cloud-word-1 {
	--color-1: #df8453;
	--color-2: #3d8dae;
	--color-3: #e4a9a8;
}

.cloud-word-2 {
	--color-1: #dbad4a;
	--color-2: #accfcb;
	--color-3: #17494d;
}

.cloud-word-3 {
	--color-1: #accfcb;
	--color-2: #e4a9a8;
	--color-3: #accfcb;
}

.cloud-word-4 {
	--color-1: #3d8dae;
	--color-2: #df8453;
	--color-3: #e4a9a8;
}

@keyframes color-animation {
	0% {
		color: var(--color-1);
	}
	32% {
		color: var(--color-1);
	}
	33% {
		color: var(--color-2);
	}
	65% {
		color: var(--color-2);
	}
	66% {
		color: var(--color-3);
	}
	99% {
		color: var(--color-3);
	}
	100% {
		color: var(--color-1);
	}
}
</style>
