<template>
  <div class="flex flex-col items-center w-full mt-20">
    <div class="w-4/5 mt-6">
      <div class="">
        <div class="text-xl">15 Search Results for Subway</div>
      </div>

      <div class="grid grid-cols-5 gap-12 mt-4">
        <div v-for="i in 15" :key="i" class="">
          <div class="bg-[#c4c4c4] h-44 rounded-lg"></div>

          <div class="mt-3 text-black">
            <div
              class="inline-flex px-2 py-px text-xs text-black rounded-sm  bg-app-gray-100"
            >
              <span class="inline-block mr-1">
                <MaterialIcon icon="emoji_events" class="text-xs" />
              </span>

              <span class="font-bold"> TOP #{{ i }} </span>
            </div>
            <div class="mt-px">
              <p class="text-lg font-medium leading-snug">Lorem Ipsum Dolor</p>
              <p class="mt-px text-xs">
                Lorem ipsum dolor sit amet consectetur adipisicing elit...
              </p>
            </div>

            <div class="flex items-center mt-px text-black">
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
  </div>
</template>

<script>
export default {
  name: 'SearchResults',
}
</script>
