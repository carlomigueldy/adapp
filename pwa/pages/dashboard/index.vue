<template>
	<div>
		<v-container>
			<v-row>
				<v-col>
					<HomeAd />
					<v-row class="mx-auto mt-3 text-center">
						<v-col
							v-for="item in items"
							:key="item.title"
							cols="2"
						>
							<CategoryButton 
								:icon="item.icon"
								:title="item.title"
							/>
						</v-col>
					</v-row>
					<SearchTextfield />

					<v-row class="mx-auto" width="400">
						<v-col
							v-for="ad in ads" 
							:key="ad.title"
							cols="6"
						>
							<Ad 
								:title="ad.title"
								:src="ad.src"
							/>
						</v-col>
					</v-row>
				</v-col>
			</v-row>
		</v-container>
	</div>
</template>

<script>
import HomeAd from '@/components/HomeAd'
import SearchTextfield from '@/components/SearchTextfield'
import CategoryButton from '@/components/CategoryButton'
import Ad from '@/components/Ad'

export default {
	components: {
		HomeAd,
		SearchTextfield,
		CategoryButton,
		Ad,
	},

	data: () => ({
		ads: [
			{
				title: 'Bravo Beach Resort',
				src: 'https://images.pexels.com/photos/237272/pexels-photo-237272.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
			},
			{
				title: 'Alpha Beach Resort',
				src: 'https://images.pexels.com/photos/753626/pexels-photo-753626.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
			},
			{
				title: 'Charlie Resort',
				src: 'https://images.pexels.com/photos/3155666/pexels-photo-3155666.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
			},
			{
				title: 'Delta Resort',
				src: 'https://images.pexels.com/photos/338504/pexels-photo-338504.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
			}
		],
		items: [
      {
        title: 'Cars',
        icon: 'mdi-car'
      },
      {
        title: 'Jobs',
        icon: 'mdi-briefcase',
      },
      {
        title: 'Real Estate',
        icon: 'mdi-domain'
      },
      {
        title: 'Sale',
        icon: 'mdi-currency-usd'
      },
      {
        title: 'Rooms',
        icon: 'mdi-bed-empty'
      },
      {
        title: 'Anything',
        icon: 'mdi-star'
      }
    ],
	}),
}
</script>