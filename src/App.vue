<template>
	<router-view />
</template>

<script lang="ts">
import { defineComponent } from "vue"
import HelloWorld from "./components/HelloWorld.vue"

export default defineComponent({
	name: "App",
	components: {
		HelloWorld,
	},
})
</script>

<style>
#app {
	background: #121214;
	color: #a8a8b3;
	height: 100vh;
	width: 100vw;
}
</style>
