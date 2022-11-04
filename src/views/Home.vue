<template>
	<PageLayout>
		<div class="app-title">
			<h1>Welcome to the Cowpoke Lounge</h1>
		</div>
		<div>
			The world's foremost virtual resource for aficionados of all things cattle-tending related
		</div>
		<HomeItem v-for="(item, index) in items" :title="item.title" :text="item.text" :icon="item.icon"
			:color="item.color" :route="item.route" :link="item.link" :key="item.id" />
	</PageLayout>
</template>

<script lang="ts">
import HomeItem from '@/components/HomeItem.vue'
import PageLayout from '@/components/navigation/PageLayout.vue'

export default {
	name: "Home",
	components: { HomeItem, PageLayout },
	data() {
		return {
			items: [
				{
					id: 1,
					title: 'Get Started',
					text: 'Create an account for a personalized experience',
					icon: 'mdi-arrow-right-circle',
					color: 'info',
					route: { name: 'login' },
					link: ''
				},
				{
					id: 2,
					title: 'Stay Connected',
					text: 'Check out The Feed to stay up to date on all things cowpoke-related!',
					icon: 'mdi-newspaper-variant-multiple',
					color: 'warning',
					route: { name: 'feed' },
					link: ''
				},
				{
					id: 3,
					title: 'Why Cowpoke Lounge?',
					text: 'Because it\'s silly fun! Find more silliness over on GitHub',
					icon: 'mdi-github',
					color: 'secondary',
					route: undefined,
					link: 'https://github.com/adnammit'
				},
			]
		}
	},
}
</script>