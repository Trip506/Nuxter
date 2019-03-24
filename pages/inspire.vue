<template>
	<v-layout>
		<v-flex text-xs-center>
			<v-carousel>
				<v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src"></v-carousel-item>
			</v-carousel>

			<v-card>
				<v-card-title primary-title>
					<h1>Stop the construction of towers!</h1>
				</v-card-title>
				<v-card-text>
					The network comes from Almeria and the Alpujarra and crosses the Valley, cutting it in two with electrical towers of up to 80 meters. of height and bases of 250 mts. square, until you reach Granada.
					The environmental impact is incalculable. It seriously affects flora, fauna (such as raptors in the area), health (electromagnetic pollution), tourism, agriculture and economy. It will depreciate significantly the heritage of the neighbors of the Valley.
					A map of the route, and the location of the new substation:
				</v-card-text>
				<v-card-actions>
					<v-spacer/>
					<v-btn color="primary" flat nuxt to="/inspire">Continue</v-btn>
				</v-card-actions>
			</v-card>
		</v-flex>
	</v-layout>
</template>

<script>
export default {
	data() {
		return {
			items: [
				{
					src: require("@/assets/tower-construction0.jpg")
				},
				{
					src: require("@/assets/tower-construction1.jpg")
				},
				{
					src: require("@/assets/tower-construction2.jpg")
				}
				// {
				// 	src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg"
				// }
			]
		};
	}
};
</script>