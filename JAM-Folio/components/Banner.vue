<template>
	<div class="banner text-gray-100">
		<div class="container mx-auto px-4">
			<div class="grid grid-cols-5 w-full">
				<div class="left col-span-3 v-flex">
					<h1 class="text-left font-bold">
						Romain <br />
						<span class="last-name">Sanson</span>
						<span class="text-green-500">.</span>
					</h1>
					<div class="socials">
						<img src="~/assets/images/linkedin-in-brands.svg" alt="" />
						<img src="~/assets/images/github-brands.svg" alt="" />
						<img src="~/assets/images/at-solid.svg" alt="" />
					</div>
				</div>
				<div class="right col-span-2 text-left v-flex">
					<Bio />
					<div class="bubble tech rails">
						<i class="devicon-rails-plain colored"></i>
					</div>
					<div class="bubble tech vue">
						<i class="devicon-vuejs-plain colored"></i>
					</div>
					<div class="bubble tech ruby">
						<img src="~/assets/images/ruby.png" alt="" />
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.v-flex {
	display: flex;
	align-items: center;
}

.banner {
	background-color: rgb(44, 47, 50);
	position: relative;
	overflow: hidden;

	&::after {
		position: absolute;
		transform: translate(50%, 50%);
		content: '';
		bottom: 25%;
		right: 17%;
		width: 90rem;
		height: 90rem;
		border-radius: 50%;
		border: 7px solid lighten(rgba(43, 47, 49, 0.3), 5%);
	}
}

.left {
	position: relative;
	height: 28rem;

	h1 {
		position: relative;
		font-size: 6rem;
		letter-spacing: 10px;
		line-height: 5.5rem;
		z-index: 1;

		.last-name {
			letter-spacing: 23px;
		}

		&::before {
			content: '';
			background-color: #48bb78;
			height: 0.7rem;
			width: 7rem;
			position: absolute;
			bottom: -2rem;
			left: 0px;
		}

		&::after {
			content: 'fullstack developer';
			position: absolute;
			height: 0.7rem;
			bottom: 7px;
			left: 8rem;
			color: #48bb78;
			font-size: 20px;
			letter-spacing: 7px;
		}
	}

	.socials {
		position: absolute;
		left: 0px;
		bottom: 15px;
		display: flex;
		align-items: center;

		img {
			width: 2rem;
			height: 2rem;
			margin-right: 1rem;
			fill: #e2e8f0;
		}
	}
}

.right {
	height: 28rem;
	position: relative;

	.bubble {
		background-color: rgb(37, 39, 42);
		padding: 2rem;
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center;

		i {
			font-size: 6rem;
		}
	}

	.tech {
		position: absolute;
	}

	.rails {
		bottom: -20%;
		left: -40%;
		width: 200px;
		height: 200px;
		// border: 1px solid rgba(72, 187, 120, 0.6);
		// box-shadow: 0px 0px 400px 100px rgba(72, 187, 120, 0.02);
	}

	.vue {
		top: -30%;
		left: 20%;
		width: 160px;
		height: 160px;
		// border: 1px solid rgba(72, 187, 120, 0.6);
		// box-shadow: 0px 0px 300px 75px rgba(72, 187, 120, 0.02);

		i {
			margin-top: 10px;
			font-size: 5rem;
		}
	}

	.ruby {
		top: 40%;
		right: -35%;
		width: 120px;
		height: 120px;
		// border: 1px solid rgba(72, 187, 120, 0.6);
		// box-shadow: 0px 0px 200px 50px rgba(72, 187, 120, 0.02);
	}
}
</style>
