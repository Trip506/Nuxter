<template>
	<v-layout column justify-center>
		<v-flex xs12 text-xs-center>
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
		<v-spacer></v-spacer>
		<v-flex xs12 mt-5>
			<v-card>
				<v-layout row wrap align-content-space-between>
					<v-flex d-flex xs4>
						<BusinessCard c="sam" name="Sam Furneaux"></BusinessCard>
					</v-flex>
				</v-layout>
			</v-card>
		</v-flex>
	</v-layout>
</template>

<script>
import BusinessCard from "../components/BusinessCard.vue";
export default {
	components: {
		BusinessCard
	},
	data() {
		return {
			items: [
				{
					src: require("@/assets/app3.jpg")
				},
				{
					src: require("@/assets/app1.jpg")
				},
				{
					src: require("@/assets/app2.jpg")
				}
				// {
				// 	src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg"
				// }
			]
		};
	}
};
</script>