<template>
  <div
    class="
      py-8
      overflow-auto
      fixed
      z-10
      top-0
      left-0
      right-0
      bottom-0
      bg-white/70
      backdrop-blur-lg
    "
  >
    <div class="w-3/5 mx-auto">
      <div class="flex gap-6">
        <div class="flex-grow">
          <p class="text-xl font-bold">Add your review for</p>
          <div class="mt-2">
            <div
              class="
                rounded-full
                inline-flex
                pl-4
                pr-8
                pt-2
                pb-2
                border
                items-center
                shadow
                bg-white/60
              "
            >
              <div class="">
                <div
                  class="w-12 h-12 flex-shrink-0 rounded-full bg-[#c4c4c4]"
                ></div>
              </div>

              <div class="pl-4">
                <p class="text-sm font-bold leading-snug">
                  Some nice fancy restaurant
                </p>
                <div class="flex items-center text-black">
                  <span class="inline-block mr-1">
                    <MaterialIcon icon="place" class="text-xs" />
                  </span>

                  <span class="inline-block text-xs">Stoke-on-Trent, Uk</span>
                </div>
                <div class="mt-px">
                  <StarRating />
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="">
          <div
            class="
              rounded-full
              px-5
              py-3
              border border-[#c4c4c4]
              text-black text-sm
              font-bold
              leading-snug
            "
          >
            Cancel
          </div>
        </div>
      </div>

      <div class="mt-6">
        <div class="flex flex-col gap-2">
          <AStarReviewCard
            v-for="template in restaurantTemplate"
            :key="template.name"
            :template="template"
          />

          <div class="border rounded-xl px-4 py-3 shadow bg-white/60">
            <div class="">
              <p class="text-base font-bold">Rate your overall experience</p>
            </div>

            <div class="mt-4">
              <StarRating size="xl" :count="false" :tight="false" />
            </div>
          </div>

          <AStarReviewCard
            type="textarea"
            :template="{
              name: 'Do you have any other comments?',
              description:
                'Type in any special comment about your experience below',
            }"
            placeholder="Type your comments here"
          />
        </div>

        <div class="flex-col flex mt-4">
          <div
            class="
              rounded-full
              text-center
              w-full
              bg-black
              px-5
              py-3
              border border-black
              text-white text-sm
              font-bold
              leading-snug
            "
          >
            Submit Review
          </div>

          <div
            class="
              w-full
              text-center
              mt-8
              rounded-full
              px-5
              py-3
              border border-[#c4c4c4]
              text-black text-sm
              font-bold
              leading-snug
            "
          >
            Cancel
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AddReview',

  data: () => {
    return {
      restaurantTemplate: {
        typeOfService: {
          name: 'Type of Service',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, illo! Sed vitae labore',
          fields: [
            {
              name: 'FastFood',
            },
            {
              name: 'A la Carte',
            },
            {
              name: "Table D'Hote",
            },
          ],
        },
        typeOfFood: {
          name: 'Type of Food',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, illo! Sed vitae labore',
          fields: [
            {
              name: 'Asian',
            },
            {
              name: 'Caribbean',
            },
            {
              name: 'Oriental',
            },
            {
              name: 'Italian',
            },
            {
              name: 'American',
            },
            {
              name: 'Traditional',
            },
          ],
        },
        typeOfOccassion: {
          name: 'Type of Occassion',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, illo! Sed vitae labore',
          fields: [
            {
              name: 'Family Meal',
            },
            {
              name: 'Romantic Dinner',
            },
            {
              name: 'Kids Meal',
            },
            {
              name: 'Business Lunches',
            },
            {
              name: 'View',
            },
          ],
        },
        diningOptions: {
          name: 'Dining Options',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, illo! Sed vitae labore',
          fields: [
            {
              name: 'Breakfase',
            },
            {
              name: 'Lunch',
            },
            {
              name: 'Dinner',
            },
            {
              name: 'Supper',
            },
            {
              name: 'Takeout',
            },
          ],
        },
        experience: {
          name: 'General Experience',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, illo! Sed vitae labore',
          fields: [
            {
              name: 'Average expense of serving per head',
            },
            {
              name: 'Quality of food',
            },
            {
              name: 'Ambiance of the experience',
            },
            {
              name: 'Quality of service',
            },
            {
              name: 'Cleanliness',
            },
            {
              name: 'Speed of service',
            },
            {
              name: 'Value for money',
            },
            {
              name: 'Allergy information provided',
            },
          ],
        },
      },
    }
  },
}
</script>
