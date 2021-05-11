<template>
	<div class="app">
		<loyaoutHeader class="header" />
		<div class="first_screen">
			<div class="main-text">
				<h1>Lorem, ipsum dolor.</h1>
				<p>
					Lorem ipsum dolor sit amet consectetur adipisicing elit.
					Voluptate, quisquam.lorem Lorem ipsum, dolor sit amet
					consectetur adipisicing elit.
				</p>
			</div>
		</div>
		<div class="second_screen">
			<div class="kitchen">
				<h2>kitchen</h2>
				<div class="grid-item">
					<div
						class="img-item"
						v-for="item of kitchenIMG"
						:key="item.id"
					>
						<img
							:src="
								require(`@/assets/images/kitchenIMG/${item.img}`)
							"
						/>
						<!-- <img :src="item.img" /> -->
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import loyaoutHeader from './components/header.vue';

export default {
	data() {
		return {
			kitchenIMG: [
				{
					id: Math.random(),
					img: 'firstImg.jpg',
				},
				{
					id: Math.random(),
					img: '9a9678ed6f93751803141ab1fe3d0e84.jpg',
				},
				{
					id: Math.random(),
					img: 'kitchen-ideas-calderone-kitchen-006-1583960334.jpg',
				},
				{
					id: Math.random(),
					img:
						'kitchens-michael-alan-kaskel-img_0d511d8e0e77ab3a_14-3280-1-7aacee2.jpg',
				},
			],
		};
	},
	components: {
		loyaoutHeader,
	},
	methods: {},
};
</script>

<style lang="scss">
* {
	margin: 0px;
	padding: 0px;
	box-sizing: border-box;
}
.app {
	max-width: 1920px;
	margin: 0 auto;
}
.header {
	display: flex;
	justify-content: space-between;
	width: 100%;
	padding: 10px;
	position: fixed;
	z-index: 1;
	span {
		font-size: 24px;
		color: green;
		.type {
			color: black;
			font-weight: 700;
			font-size: 28px;
		}
	}
	.links {
		display: flex;
		flex-direction: column;
		text-align: right;
		a {
			padding-bottom: 5px;
			color: black;
			font-size: 18px;
			&:hover {
				color: green;
			}
		}
	}
}
.first_screen {
	display: flex;
	justify-content: center;
	flex-direction: column;
	// align-items: center;
	background-image: url('./assets/STL_Traditional+Bathroom+Design_27814191.jpg');
	background-size: cover;
	background-repeat: no-repeat;
	height: 100vh;
	padding-left: 200px;
	.main-text {
		max-width: 500px;
		h1 {
			font-size: 44px;
			text-align: left;
		}
		p {
			color: green;
			font-size: 24px;
		}
	}
}
.second_screen {
	position: absolute;
	z-index: 1;
	width: 200px;
	height: 200px;
	.img-item {
	}
}
</style>
