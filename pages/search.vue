<template>
  <div class="flex flex-col items-center w-full mt-[94px]">
    <div v-if="searching" class="my-6 text-center font-bold text-sm">
      Loading...
    </div>
    <div v-if="restaurants.length" class="w-4/5 mt-6">
      <div class="">
        <div class="text-xl">{{ restaurants.length }} Search Results</div>
      </div>

      <div class="grid grid-cols-5 gap-12 mt-4">
        <nuxt-link
          v-for="(restaurant, i) in restaurants"
          :key="i"
          :to="'/restaurant/' + restaurant._id"
          class="block hover:opacity-70"
        >
          <div class="bg-[#c4c4c4] h-44 rounded-lg relative overflow-hidden">
            <img
              class="absolute object-cover w-full h-full"
              :src="'https://images.pexels.com/photos/1267315/pexels-photo-1267315.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500'"
            />
          </div>

          <div class="mt-3 text-black">
            <div
              class="
                inline-flex
                px-2
                py-px
                text-xs text-black
                rounded-sm
                bg-app-gray-100
              "
            >
              <span class="inline-block mr-1">
                <MaterialIcon icon="emoji_events" class="text-xs" />
              </span>

              <span class="font-bold"> TOP #{{ i + 1 }} </span>
            </div>
            <div class="mt-px">
              <p class="text-lg font-medium leading-snug">
                {{ restaurant.name }}
              </p>
              <div class="mt-px text-xs">
                <div class="">
                  <StarRating
                    :count="
                      restaurant.reviews ? restaurant.reviews.length : false
                    "
                    :values="overall(restaurant).rating"
                  />
                </div>
              </div>
            </div>

            <div class="flex items-center mt-px text-black">
              <span class="inline-block mr-1">
                <MaterialIcon icon="place" class="text-xs" />
              </span>

              <span class="inline-block text-xs">{{
                restaurant.location
              }}</span>
            </div>

            <div class="mt-px">
              <StarRating :values="[]" />
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>
    <div v-else-if="!searching" class="my-6 text-center font-bold text-sm">
      No search result
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchResults',

  computed: {
    searching() {
      return this.$store.state.searching
    },

    restaurants() {
      return this.$store.state.restaurants
    },

    overall() {
      return (restaurant) => {
        let overall = {}
        restaurant.ratings.forEach((rating) => {
          if (rating.name === 'Overall Delivery') overall = rating
        })

        return overall
      }
    },
  },
}
</script>
