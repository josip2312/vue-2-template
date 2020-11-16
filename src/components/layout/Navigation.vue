<template>
	<nav class="nav">
		<router-link :to="{ name: 'Index' }" class="nav-link" href="#"
			>Home
		</router-link>
		<router-link :to="{ name: 'About' }" class="nav-link" href="#"
			>About
		</router-link>
	</nav>
</template>

<script>
export default {
	name: "Navigation",
};
</script>

<style lang="scss" scoped>
.nav {
	display: flex;
	align-items: center;

	& > * + * {
		margin-left: 2.5rem;
	}

	.nav-link {
		position: relative;
		padding: 0.5rem 1rem;
	}
	.nav-link:hover {
		text-decoration: underline;
	}
	.nav-link::after {
		content: "";
		position: absolute;
		left: 0;
		bottom: 0;
		width: 100%;
		height: 0.2rem;
		background-color: var(--secondary-400);
		border-radius: 0.5rem;

		transform-origin: left;
		transition: transform 250ms ease-in-out;
		transform: scaleX(0);
	}
	.router-link-exact-active::after {
		transform: scaleX(1);
	}
}
</style>