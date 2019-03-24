<template>
	<v-layout column justify-center align-center>
		<v-flex xs12 sm8 md6>
			<div class="text-xs-center"></div>
			<v-img fluid height="400" :src="require('@/assets/towers2.jpg')"></v-img>
			<v-card>
				<!-- <v-card-title class="headline">Protecting our future</v-card-title> -->
				<v-card-text>
					<h1>Stop the destruction of mother earth in the Alpujarra</h1>
					<p>
						We must take action to stop construction of a highway of high voltage electricity towers that will cut through the beautiful Alpujarras. The devastation to the special environment, people and economy has been grossly underestimated by the pro t driven electrical giant, Red Electrica (REE).
						This is being sold as a “green” scheme to boost progress, but in reality is destroying thousands of km of land, to transport electricity all the way from France to southern Spain & Morocco, and back again. Many people live in areas that REE claims are uninhabited, soon to be inundated by giant high voltage towers and tension cables. REE has been planning this for 15 years, but only released limited details to the public recently, allowing little time to oppose the scheme! Why here? Its the cheapest
						route for REE, but the people, tourism industry, and natural beauty of the area will pay the price if this horri c scheme is to go ahead!
					</p>
				</v-card-text>
				<v-card-actions>
					<v-spacer/>
					<v-btn color="primary" flat nuxt to="/inspire">Continue</v-btn>
				</v-card-actions>
			</v-card>
			<v-flex xs12>
				<grids props="towers"></grids>
			</v-flex>
			<v-flex xs12>
				<v-card color="white">
					<v-toolbar color="info">
						<h3>Upcoming events</h3>
					</v-toolbar>
					<calendar></calendar>
				</v-card>
			</v-flex>
		</v-flex>
	</v-layout>
</template>

<script>
import Logo from "~/components/Logo.vue";
import grids from "../components/grids.vue";
import Calendar from "../components/Calendar.vue";
import VuetifyLogo from "~/components/VuetifyLogo.vue";

export default {
	components: {
		grids,
		Calendar
	}
};
</script>
