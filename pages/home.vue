<template>
  <div>
    <div class="bg-[#c4c4c4] py-28 flex justify-center mt-[94px]">
      <div class="flex flex-col items-center justify-center w-4/5 text-black">
        <div class="text-center">
          <p class="text-4xl">We Direct you to the</p>
          <p class="mt-2 font-bold text-8xl">Right Restaurant</p>
        </div>

        <div class="w-3/5 mt-6 text-center">
          <p class="text-sm">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Reprehenderit exercitationem molestias unde nisi tempore laborum
            sint veniam in aperiam. Tenetur pariatur quos eveniet praesentium,
            assumenda libero officia et facilis cupiditate.
          </p>

          <div class="flex justify-center gap-3 mt-6">
            <div
              class="
                px-5
                py-3
                text-sm
                font-bold
                leading-snug
                text-black
                border border-black
                rounded-full
              "
            >
              Create Account
            </div>

            <div
              class="
                px-5
                py-3
                text-sm
                font-bold
                leading-snug
                text-black
                border border-black
                rounded-full
              "
            >
              Login
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="relative w-4/5 mx-auto top-[-90px]">
      <div class="">
        <div class="text-xl">Browse Restaurants</div>
      </div>

      <div class="flex flex-col gap-3 mt-6">
        <div
          v-for="i in 6"
          :key="i"
          class="overflow-hidden bg-white border rounded-xl"
        >
          <div
            class="
              px-3
              py-1
              text-xs
              font-bold
              bg-[#c4c4c4] bg-opacity-25
              uppercase
              border-b
            "
          >
            #1 in top restaurants
          </div>

          <div class="px-5 py-5">
            <div class="flex gap-5">
              <div class="w-3/5">
                <div class="flex">
                  <div
                    class="w-10 h-10 bg-[#c4c4c4] overflow-hidden rounded-full"
                  ></div>
                  <div class="flex-grow pl-2">
                    <p class="text-sm font-medium leading-snug">
                      Some nice fancy restaurant
                    </p>
                    <div class="flex items-center text-black">
                      <span class="inline-block mr-1">
                        <MaterialIcon icon="place" class="text-xs" />
                      </span>

                      <span class="inline-block text-xs"
                        >Stoke-on-Trent, Uk</span
                      >
                    </div>
                  </div>
                </div>

                <div class="mt-3 text-sm">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Laboriosam optio quo vero est magni, sint sed sunt atque
                  recusandae, ex eaque quidem voluptatem exercitationem mollitia
                  totam deleniti nemo excepturi error.<br />
                </div>
              </div>
              <div class="flex flex-col w-2/5 gap-1">
                <div v-for="i in 6" :key="i" class="flex justify-between">
                  <p class="flex-grow text-xs leading-snug">Lorem Ipsum</p>
                  <StarRating :count="false" />
                </div>
              </div>
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
