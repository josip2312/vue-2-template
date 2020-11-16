<template>
	<div id="app">
		<TheHeader />
		<router-view />
		<TheFooter />
	</div>
</template>
<script>
import TheHeader from "@/components/layout/TheHeader";
import TheFooter from "@/components/layout/TheFooter";

export default {
	name: "App",
	components: {
		TheHeader,
		TheFooter,
	},
};
</script>
<style lang="scss">
@import "@/assets/sass/app.scss";
</style>
