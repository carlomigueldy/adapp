<template>
	<v-card>
		<v-img
			:src="src"
			class="white--text align-end"
			gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
			height="200px"
		>
			<v-card-title v-text="title"></v-card-title>
		</v-img>
		<v-card-actions>
			<v-spacer></v-spacer>

			<v-btn 
				v-if="!liked"
				@click="liked = true" 
				icon
			>
				<v-icon>mdi-heart-outline</v-icon>
			</v-btn>
			<v-btn
				v-else
				@click="liked = false"
				icon
			>
				<v-icon color="red">mdi-heart</v-icon>
			</v-btn>
		</v-card-actions>
	</v-card>
</template>

<script>
export default {
	props: {
		title: String,
		src: String,
	},

	data: () => ({
		liked: false,
	})
}
</script>