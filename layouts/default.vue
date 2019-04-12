<template>
	<v-app dark>
		<v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app>
			<v-list>
				<v-list-tile v-for="(item, i) in items" :key="i" :to="item.to" router exact>
					<v-list-tile-action>
						<v-icon>{{ item.icon }}</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title v-text="item.title"/>
					</v-list-tile-content>
				</v-list-tile>
			</v-list>
		</v-navigation-drawer>
		<v-toolbar :clipped-left="clipped" fixed app>
			<v-toolbar-side-icon @click="drawer = !drawer"/>
			<v-btn icon @click.stop="miniVariant = !miniVariant">
				<v-icon>{{ `chevron_${miniVariant ? 'right' : 'left'}` }}</v-icon>
			</v-btn>
			<v-btn icon @click.stop="clipped = !clipped">
				<v-icon>web</v-icon>
			</v-btn>
			<v-btn icon @click.stop="fixed = !fixed">
				<v-icon>remove</v-icon>
			</v-btn>

			<v-img fluid height="40" width="10" max-width="40" src="/faticon.ico" @click="go('/')"></v-img>

			<v-toolbar-title style="cursor:pointer;" @click="go('/')" v-text="title"/>
			<h1>{{route}}</h1>
			<v-spacer/>
			<v-btn icon @click.stop="rightDrawer = !rightDrawer">
				<v-icon>menu</v-icon>
			</v-btn>
		</v-toolbar>
		<v-content>
			<v-container>
				<nuxt/>
			</v-container>
		</v-content>
		<v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
			<v-list>
				<v-list-tile @click.native="right = !right">
					<v-list-tile-action>
						<v-icon light>compare_arrows</v-icon>
					</v-list-tile-action>
					<v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
				</v-list-tile>
			</v-list>
		</v-navigation-drawer>

		<Footer></Footer>
	</v-app>
</template>

<script>
import Footer from "../components/Footer.vue";
export default {
	components: {
		Footer
	},
	data() {
		return {
			clipped: false,
			drawer: false,
			fixed: false,
			items: [
				{
					icon: "apps",
					title: "Welcome",
					to: "/"
				},
				{
					icon: "bubble_chart",
					title: "Inspire",
					to: "/inspire"
				},
				{
					icon: "image",
					title: "Gallery",
					to: "/gallery"
				},
				{
					icon: "print",
					title: "Posters",
					to: "/posters"
				},
				{
					icon: "info",
					title: "Morocco",
					to: "/morocco"
				}
			],

			miniVariant: false,
			right: true,
			rightDrawer: false,
			title: "DI NO A LAS TORRES"
		};
	},
	methods: {
		go(route) {
			this.$router.push(route);
		}
		// route() {
		// 	return this.$route.name;
		// }
	}
};
</script>
