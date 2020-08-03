<template>
	<div class="slider">
		<div v-for="work in works">
			<transition :name="direction == 'horizontal' ? 'h-slide' : 'v-slide'">
				<div
					v-if="work === works[currentId]"
					class="slide"
					:style="{
						backgroundImage:
							'url(' +
							`http://localhost:1337${work.image.formats.large.url}` +
							')'
					}"
				>
					{{ work.title }}
				</div>
			</transition>
		</div>
	</div>
</template>

<script>
export default {
	props: ['direction', 'delay', 'startId', 'works'],
	data() {
		return {
			currentId: this.startId
		};
	},
	methods: {
		initSlider() {
			setInterval(() => {
				this.currentId === this.works.length - 1
					? (this.currentId = 0)
					: this.currentId++;
			}, 5000);
		}
	},
	mounted() {
		setTimeout(() => {
			this.initSlider();
		}, this.delay);
	}
};
</script>

<style lang="scss" scoped>
.slider {
	position: relative;
	width: 100%;
	height: 100%;
	display: flex;
	align-items: center;
	justify-content: center;
	overflow: hidden;

	.slide {
		position: absolute;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		display: flex;
		align-items: center;
		justify-content: center;
		color: white;
		background-position: center;
		background-size: cover;
	}
}

.h-slide-enter-active {
	animation: horzontalSlideIn 2s;
}
.h-slide-leave-active {
	animation: horzontalSlideOut 2s;
}

@keyframes horzontalSlideIn {
	0% {
		transform: translateX(100%);
	}

	100% {
		transform: translateX(0%);
	}
}

@keyframes horzontalSlideOut {
	0% {
		transform: translateX(0%);
	}

	100% {
		transform: translateX(-100%);
	}
}

.v-slide-enter-active {
	animation: verticalSlideIn 2s;
}
.v-slide-leave-active {
	animation: verticalSlideOut 2s;
}

@keyframes verticalSlideIn {
	0% {
		transform: translateY(100%);
	}

	100% {
		transform: translateY(0%);
	}
}

@keyframes verticalSlideOut {
	0% {
		transform: translateY(0%);
	}

	100% {
		transform: translateY(-100%);
	}
}
</style>
