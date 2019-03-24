<template>
	<v-hover>
		<v-card slot-scope="{ hover }" class="mx-auto" color="grey lighten-4" max-width="600">
			<v-img :aspect-ratio="16/9" :src="require('@/assets/tower-construction0.jpg')">
				<v-expand-transition>
					<div
						v-if="hover"
						class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
						style="height: 100%;"
					>sunset</div>
				</v-expand-transition>
			</v-img>
			<v-card-text class="pt-4" style="position: relative;">
				<v-btn absolute color="orange" class="white--text" fab large right top>
					<v-icon>mdi-cart</v-icon>
				</v-btn>
				<div class="font-weight-light grey--text title mb-2">Bayacas, Orgiva</div>
				<h3 class="display-1 font-weight-light orange--text mb-2">Fight to protect nature</h3>
				<div
					class="font-weight-light title mb-2"
				>Showing community solidary against faceless corporations
					<br>Made of bamboo by hand
				</div>
			</v-card-text>
		</v-card>
	</v-hover>
</template>

<style>
.v-card--reveal {
	align-items: center;
	bottom: 0;
	justify-content: center;
	opacity: 0.5;
	position: absolute;
	width: 100%;
}
</style>


