<template>
	<div class="works">
		<div class="container">
			<div class="grid grid-cols-3 gap-4">
				<div class="col-span-1">
					<Slider
						:direction="'vertical'"
						:delay="500"
						:startId="0"
						:works="works"
					/>
				</div>
				<div class="col-span-2 row-span-2">
					<Slider
						:direction="'horizontal'"
						:delay="250"
						:startId="1"
						:works="works"
					/>
				</div>
				<div class="col-span-1">
					<Slider
						:direction="'horizontal'"
						:delay="100"
						:startId="2"
						:works="works"
					/>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from 'axios';
export default {
	data() {
		return {
			works: []
		};
	},
	methods: {
		async getWorks() {
			let works = await axios.get(`http://localhost:1337/works`);
			this.works = works.data;
		}
	},
	mounted() {
		this.getWorks();
	}
};
</script>

<style scoped lang="scss">
.works {
	background-color: rgb(36, 38, 41);
	.grid {
		width: 80%;
		height: 60vh;
	}
}
</style>
