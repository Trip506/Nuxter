<template>
	<v-layout mt-5 mb-5>
		<v-flex xs12>
			<v-toolbar color="alert" dark>
				<v-toolbar-side-icon></v-toolbar-side-icon>
				<v-toolbar-title>Media</v-toolbar-title>
				<v-spacer></v-spacer>
				<v-btn icon>
					<v-icon>search</v-icon>
				</v-btn>
			</v-toolbar>

			<v-card>
				<v-container fluid grid-list-md>
					<v-layout row wrap>
						<v-flex v-for="(card, i) in cards" v-bind="{ [`xs${card.flex}`]: true }" :key="card.title">
							<v-card>
								<v-img :src="require('@/assets/'+props+i+'.jpg')" height="200px">
									<v-container fill-height fluid pa-2>
										<v-layout fill-height>
											<v-flex xs12 align-end flexbox>
												<span class="headline white--text" v-text="card.title"></span>
											</v-flex>
										</v-layout>
									</v-container>
								</v-img>

								<v-card-actions>
									<v-spacer></v-spacer>
									<v-btn icon>
										<v-icon>favorite</v-icon>
									</v-btn>
									<v-btn icon>
										<v-icon>bookmark</v-icon>
									</v-btn>
									<v-btn icon>
										<v-icon>share</v-icon>
									</v-btn>
								</v-card-actions>
							</v-card>
						</v-flex>
					</v-layout>
				</v-container>
			</v-card>
		</v-flex>
	</v-layout>
</template>

<script>
export default {
	props: ["props"],
	data: () => ({
		cards: [
			{
				title: "Pylons souring over Rio Chico",
				src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
				flex: 12
			},
			{
				title: "Sam",
				src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
				flex: 6
			},
			{
				title: "Sivan ",
				src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
				flex: 6
			}
		]
	})
};
</script>
