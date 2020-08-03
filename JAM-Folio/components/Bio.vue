<template>
	<div class="bio-card">
		<h1 class="font-bold">
			Freelance Full Stack Web Developer
			<span class="text-green-500">&</span> Website Designer
		</h1>
		<p class="text-lg font-medium text-gray-500">
			Développeur full-stack, je vous accompagne dans la réalisation de vos
			projets web, de la mise en place d’une simple landing page à la création
			d’un portfolio, d’un site e-commerce, d’un site vitrine Wordpress ou d’une
			application web complète en Ruby on Rails.
		</p>
		<a href="" class="contact-btn">contact me</a>
	</div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.bio-card {
	padding: 4rem 0rem 4rem 3.8rem;
	border-radius: 0.3rem;

	h1 {
		font-size: 2rem;
		line-height: 2.2rem;
		padding-bottom: 1rem;
	}

	p {
		text-align: justify;
	}

	.contact-btn {
		position: absolute;
		left: 3.7rem;
		bottom: 15px;
		color: #48bb78;
		font-size: 2rem;
		letter-spacing: 3px;
	}
}
</style>
