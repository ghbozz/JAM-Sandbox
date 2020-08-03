<template>
	<div class="nav">
		<div class="wrapper mx-auto px-4">
			<span class="logo text-5xl">logo</span>
			<div class="menu text-3xl">
				<a href="#">See my work</a>
			</div>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.nav {
	z-index: 2;
	position: absolute;
	display: flex;
	align-items: center;
	height: 4rem;
	width: 100%;
	color: white;

	.wrapper {
		width: 100%;
		height: 100%;
		margin: 0 auto;
		display: flex;
		justify-content: space-between;
		align-items: center;
		text-align: center;
		max-width: 1280px;

		.menu {
			a {
				margin-right: 2rem;

				&:last-child {
					margin-right: 0px;
				}
			}
		}
	}
}
</style>
