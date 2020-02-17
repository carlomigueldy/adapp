<template>
	<div>
		<v-btn
			fab
		>
			<v-icon>{{ icon }}</v-icon>
		</v-btn>
	</div>
</template>

<script>
export default {
  props: {
	icon: String,
	title: String,
  }
}
</script>