<template>
	<header>
		<div class="container">
			<router-link :to="{ name: 'Index' }" class="logo">Logo</router-link>
			<Navigation />
		</div>
	</header>
</template>

<script>
import Navigation from "@/components/layout/Navigation";
export default {
	name: "TheHeader",
	components: {
		Navigation,
	},
};
</script>

<style lang="scss" scoped>
.header {
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
}
.container {
	display: flex;
	align-items: center;
	justify-content: space-between;
	.logo {
		padding: 1.5rem 0;
	}
}
</style>