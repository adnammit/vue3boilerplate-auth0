<template>
	<v-card class="ma-6">
		<v-card-title>
			{{ title }}
		</v-card-title>

		<v-card-text>
			<v-row align="center" class="px-2" hide-gutters no-gutters>
				<v-col cols="8">
					{{ text }}
				</v-col>
				<v-col align="right">
					<v-btn v-if="link != ''" class="ma-2 color--bold" :color="color" :icon="icon" size="x-large" :href="link"></v-btn>
					<v-btn v-else class="ma-2 color--bold" :color="color" :icon="icon" size="x-large" :to="route"></v-btn>
				</v-col>
			</v-row>
		</v-card-text>
	</v-card>
</template>

<script setup lang="ts">
defineProps({
	title: String,
	text: String,
	icon: String,
	color: String,
	route: Object,
	link: String
})
</script>