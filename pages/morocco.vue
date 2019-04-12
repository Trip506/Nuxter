<template>
	<v-container grid-list-sm>
		<v-layout row wrap>
			<v-flex xs12>
				<h1>Whats the deal with Morcco?</h1>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
			</v-flex>
			<v-flex xs12>
				<v-timeline>
					<v-timeline-item large>
						<template v-slot:icon>
							<v-avatar>
								<img :src="require('@/assets/morocco.png')">
							</v-avatar>
						</template>
						<template v-slot:opposite>
							<span>Morocco</span>
						</template>
						<v-card class="elevation-2">
							<v-card-title class="headline">Dirty energy</v-card-title>
							<v-card-text>Supplies Spain with renewable energy while building coal power stations for it's people</v-card-text>
						</v-card>
						<v-card-media height="200px" :src="require('@/assets/factory.jpg')"></v-card-media>
					</v-timeline-item>
					<v-timeline-item large>
						<template v-slot:icon>
							<v-avatar>
								<img :src="require('@/assets/spain.png')">
							</v-avatar>
						</template>
						<template v-slot:opposite>
							<span>Spain</span>
						</template>
						<v-card class="elevation-2">
							<v-card-title class="headline">Fooling us all</v-card-title>
							<v-card-text>
								Supplies France with renewable energy so France
								can meet it's EU quota
							</v-card-text>
						</v-card>
						<v-card-media height="200px" :src="require('@/assets/pylons.jpg')"></v-card-media>
					</v-timeline-item>
					<v-timeline-item large>
						<template v-slot:icon>
							<v-avatar>
								<img :src="require('@/assets/france.png')">
							</v-avatar>
						</template>
						<template v-slot:opposite>
							<span>France</span>
						</template>
						<v-card class="elevation-2">
							<v-card-title class="headline">Profiting from it all</v-card-title>
							<v-card-text>Produces cheap nuclear power for export abroad</v-card-text>
						</v-card>
						<v-card-media height="200px" :src="require('@/assets/nuclear.jpg')"></v-card-media>
					</v-timeline-item>
				</v-timeline>
			</v-flex>
			<v-card>
				<v-card-text>Morocco wants to build solar plants specifically for export to Europe. However, Morocco's own power supply is to be covered by two gigantic coal-fired power plants in the north of the country, with one power station already completed and another in plan . The coal for this is imported by ship to Morocco. The Safi Power Station is so large that it alone covers 25% of the country's energy needs. This is a lucrative business model for the Moroccan Kingdom. The flow of coal is very cheap for Morocco, since the African country, unlike EU member states, does not have to pay a CO2-tax to the EU.</v-card-text>
				<v-card-text>
					<b>In essence, Spain and France are outsourcing dirty coal fired energy production to countries with less environmental laws and regulations</b>
				</v-card-text>
			</v-card>

			<v-flex mt-5 xs12>
				<v-card>
					<v-card-title primary-title>
						<h2>Safi Coal Power Station Morocco</h2>
					</v-card-title>
					<v-card-media height="300" :src="require('@/assets/stationmap.png')"></v-card-media>
					<v-container grid-list-md text-xs-center>
						<v-layout row wrap>
							<v-flex xs4>
								<v-avatar size="100" color="red">
									<img :src="require('@/assets/power.png')" alt="alt">
								</v-avatar>
								<v-card-text>
									<h3>25%</h3>of Morocco's domestic energy demand is provided by this one power station
								</v-card-text>
							</v-flex>
							<v-flex xs4>
								<v-avatar size="100" color="red">
									<img :src="require('@/assets/coal.png')" alt="alt">
								</v-avatar>
								<v-card-text>
									<h3>3,000,000 tonnes</h3>Coal imported for the
									power station per year
								</v-card-text>
							</v-flex>
							<v-flex xs4>
								<v-avatar size="100" color="red">
									<img :src="require('@/assets/ship.png')" alt="alt">
								</v-avatar>

								<v-card-text>
									<h3>7,000,000 tonnes</h3>Coal import capacity to meet needs of second planned power station
								</v-card-text>
							</v-flex>
						</v-layout>
					</v-container>
					<v-card-media height="auto" :src="require('@/assets/safi.png')"></v-card-media>
				</v-card>
			</v-flex>

			<v-flex xs12>
				<v-card-text>
					EU directive is that by 2020 each member state in its total balance at least 20% of electricity from renewable energy sources.
					This is a problem especially in France, whose energy supply consists of more than 70% of nuclear power. In order to reach the 20% mark on time, France has an interest in importing green electricity from Spain and profitably exporting the superfluous nuclear power. The target total balance of 20% green electricity is thus achieved - at least on paper.
				</v-card-text>
				<v-card-text>
					<b>Not only does Morocco and France benefit from the export of green electricity, but above all the REE company - from the supply of the necessary electricity grids.</b>
				</v-card-text>
				<v-card-text>
					<h3>Red electrica is building a third undersee cable, this one of 400kv to transport renewable energy from Morocco, costing €150,000,000 and funded 50/50 by Spain and Morocco</h3>
				</v-card-text>
			</v-flex>
		</v-layout>
	</v-container>
</template>


<script>
import SafiEnergyCompany from "../components/SafiEnergyCompany.vue";
export default {
	components: {
		SafiEnergyCompany
	}
};
</script>

<style>
</style>
