<template>
	<v-layout>
		<v-flex xs12>
			<v-img :src="require('../assets/app'+img+'.jpg')"></v-img>
		</v-flex>
		<v-flex xs12 sm6>
			<v-container grid-list-sm fluid>
				<!-- <v-img :src="require('../assets/app'+img+'.jpg')"></v-img> -->
				<v-layout row wrap>
					<v-flex v-for="n in 9" :key="n" xs4 d-flex @click="setImg(n)">
						<v-img
							v-model="img"
							:src="require('@/assets/app' + n + '.jpg')"
							:lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
							aspect-ratio="1"
							class="grey lighten-2"
						>
							<template v-slot:placeholder>
								<v-layout fill-height align-center justify-center ma-0>
									<v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
								</v-layout>
							</template>
						</v-img>
					</v-flex>
				</v-layout>
			</v-container>
		</v-flex>
	</v-layout>
</template>

<script>
export default {
	data: () => ({
		img: "1"
	}),
	methods: {
		setImg(src) {
			this.img = src;
		}
	}
};
</script>
