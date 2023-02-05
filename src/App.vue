<template>
	<div id="app">
		<div class="cat-container">
			<CatHead></CatHead>
			<CatBody></CatBody>
			<CatBall></CatBall>
			<CatCloud v-if="showInfo"></CatCloud>
		</div>
		<div class="button-container">
			<CloudButton @switch-visibility="switchVisibility"></CloudButton>
		</div>
	</div>
</template>

<script>
import Background from './components/Background.vue';
import CatHead from './components/CatHead.vue';
import CatBody from './components/CatBody.vue';
import CatBall from './components/CatBall.vue';
import CatCloud from './components/CatCloud.vue';
import CloudButton from './components/CloudButton.vue';

export default {
	name: 'App',
	components: {
		Background,
		CatHead,
		CatBody,
		CatBall,
		CatCloud,
		CloudButton,
	},

	data() {
		return {
			showInfo: false,
		};
	},

	methods: {
		switchVisibility() {
			this.showInfo = !this.showInfo;
		},
	},
};
</script>

<style>
.cat-container {
	height: 600px;
	width: 600px;
	position: absolute;
	transform: translate(-50%, -50%);
	left: 30%;
	top: 75%;
}

.button-container {
	height: 200px;
	width: 200px;
	position: absolute;
	transform: translate(-50%, -50%);
	left: 50%;
	top: 35%;
}
</style>
