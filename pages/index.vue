<template>
  <div class="w-full mt-40 flex flex-col items-center">
    <div class="text-center text-black">
      <p class="text-6xl">Find a Restaurant</p>

      <div class="flex justify-center">
        <p class="text-sm mt-3 w-2/4">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Non
          reiciendis ad voluptas? Rerum animi est, suscipit nemo eveniet culpa
          consequatur, similique sequi distinctio quibusdam, repellendus
          incidunt doloribus! Error, repellat tempora.
        </p>
      </div>
    </div>

    <div class="w-3/5 mt-4">
      <div class="relative bg-[#e7e7e7] rounded-full w-full flex">
        <div
          class="
            px-6
            py-4
            flex
            items-center
            justify-center
            flex-grow-0
            text-[#626161]
          "
        >
          <MaterialIcon class="text-xl" icon="filter_alt" />
        </div>

        <input
          type="text"
          class="
            py-4
            block
            h-full
            flex-grow
            text-xl
            focus:outline-none
            text-[#626161]
            bg-[#e7e7e7]
          "
          placeholder="Find a restaurant"
        />

        <div
          class="
            px-6
            py-4
            flex
            items-center
            justify-center
            flex-grow-0
            text-[#626161]
          "
        >
          <MaterialIcon class="text-2xl" icon="search" />
        </div>
      </div>
    </div>

    <div class="mt-4 text-center text-lg">
      Don't have any in mind?
      <span class="underline">View all restaurants</span>
    </div>

    <div class="mt-6 w-4/5">
      <div class="flex justify-between items-center">
        <div class="text-xl">Featured Restaurants</div>

        <div class="flex items-center">
          <div class="pr-4 text-base leading-none">See all restaurants</div>

          <span class="">
            <MaterialIcon icon="arrow_forward_ios" class="text-lg" />
          </span>
        </div>
      </div>

      <div class="grid grid-cols-5 gap-12 mt-4">
        <div v-for="i in 5" :key="i" class="">
          <div class="bg-[#c4c4c4] h-44 rounded-lg"></div>

          <div class="mt-3 text-black">
            <div class="">
              <p class="text-lg font-medium leading-snug">Lorem Ipsum Dolor</p>
              <p class="text-xs mt-px">
                Lorem ipsum dolor sit amet consectetur adipisicing elit...
              </p>
            </div>

            <div class="mt-px flex items-center text-black">
              <span class="inline-block mr-1">
                <MaterialIcon icon="place" class="text-xs" />
              </span>

              <span class="inline-block text-xs">Stoke-on-Trent, Uk</span>
            </div>

            <div class="mt-px">
              <StarRatings />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LandingPage',
}
</script>
