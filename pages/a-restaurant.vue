<template>
  <div>
    <div class="mt-[110px] relative w-4/5 mx-auto">
      <div class="flex">
        <div class="featured-image flex-shrink-0 rounded-xl bg-[#c4c4c4]"></div>

        <div class="pl-5">
          <div class="">
            <p class="text-3xl font-bold leading-snug text-black">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit
            </p>
            <p class="pt-2 text-sm leading-snug text-black">
              Lorem ipsum dolor, sit amet consectetur adipisicing elit.
              Excepturi magnam ex aliquid eius eaque natus non corrupti possimus
              reiciendis sed doloribus provident tempora dolore voluptatibus, ea
              repudiandae expedita pariatur cupiditate. Lorem ipsum dolor, sit
              amet consectetur adipisicing elit. Excepturi magnam ex aliquid
              eius eaque natus non corrupti possimus reiciendis sed doloribus
              provident tempora dolore voluptatibus, ea repudiandae expedita
              pariatur cupiditate.<br />
              Lorem ipsum dolor, sit amet consectetur adipisicing elit.
              Excepturi magnam ex aliquid eius eaque natus non corrupti possimus
              reiciendis sed doloribus provident tempora dolore voluptatibus, ea
              repudiandae expedita pariatur cupiditate.
            </p>
          </div>

          <div class="mt-4">
            <p class="text-lg font-bold">Ratings</p>

            <div class="flex flex-col gap-1 mt-2 w-3/4">
              <div
                v-for="i in 6"
                :key="i"
                class="flex justify-between items-center"
              >
                <p class="flex-grow text-xs leading-snug">Lorem Ipsum</p>
                <StarRating :count="false" size="md" />
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="mt-10">
        <div class="flex">
          <div class="text-black flex-grow">
            <p class="text-lg font-bold">Add your review</p>
            <div class="mt-1 text-sm">
              To add a review, you need to have an existing account. Dont have?
              Create an account
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
              Add your review
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="relative w-4/5 mt-10 mx-auto">
      <div class="">
        <div class="text-xl">4 Reviews</div>
      </div>

      <div class="flex flex-col gap-3 mt-6">
        <div
          v-for="i in 6"
          :key="i"
          class="overflow-hidden bg-white border rounded-xl"
        >
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
  name: 'ARestaurant',
}
</script>

<style lang="postcss" scoped>
.featured-image {
  width: calc(100vh - 130px);
  padding-bottom: calc(100vh - 130px);
}
</style>
