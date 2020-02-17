<template>
	<div>
		<v-card color="indigo darken-1" tile flat dark>
			<v-card-title >
				<v-row>
					<v-col  justify="center" align="center" cols="5">
						<v-avatar size="128">
							<img 
								src="https://i.pravatar.cc/150?img=32"
								alt="Avatar"
							/>
						</v-avatar>
					</v-col>
					<v-col cols="7">
						<div class="title">Kate</div>
						<v-rating
							v-model="rating"
							color="yellow darken-3"
							background-color="grey darken-1"
							empty-icon="$ratingFull"
							half-increments
							hover
						></v-rating>
						<div class="subtitle-2">
							Baligya * Halin * Wala
						</div>
					</v-col>
				</v-row>
			</v-card-title>

			<v-tabs
				v-model="tab"
				background-color="transparent"
				centered
			>
				<v-tab
					v-for="item in items"
					:key="item"
				>
					{{ item }}
				</v-tab>
			</v-tabs>

			<v-tabs-items v-model="tab">
				<v-tab-item>
					<v-container>
						<v-row>
							<v-col cols="6">
								<Ad 
									:title="ads[0].title"
									:src="ads[0].src"
								/>
							</v-col>
							<v-col cols="6">
								<Ad 
									:title="ads[1].title"
									:src="ads[1].src"
								/>
							</v-col>
						</v-row>
					</v-container>
				</v-tab-item>
				<v-tab-item>

				</v-tab-item>
				<v-tab-item>

				</v-tab-item>
			</v-tabs-items>
		</v-card>
	</div>
</template>

<script>
import Ad from '@/components/Ad'

export default {
	components: {
		Ad,
	},
	
	data () {
		return {
			tab: null,
			rating: 4.5,
			items: [
				'Listings', 'Favorites', 'Sold'
			],
			ads: [
				{
					title: 'Bravo Beach Resort',
					src: 'https://images.pexels.com/photos/237272/pexels-photo-237272.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
				},
				{
					title: 'Delta Resort',
					src: 'https://images.pexels.com/photos/338504/pexels-photo-338504.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
				}
			],
		}
	},
}
</script>