<template>
  <div class="min-h-screen">
    <div
      class="fixed top-0 left-0 z-10 flex justify-center w-full py-6 bg-white"
    >
      <div class="flex justify-between w-4/5">
        <div class="w-2/5">
          <div class="relative bg-[#e7e7e7] rounded-full w-full h-full flex">
            <div
              class="
                px-5
                py-3
                flex
                items-center
                justify-center
                flex-grow-0
                text-[#626161]
              "
            >
              <MaterialIcon class="text-sm" icon="filter_alt" />
            </div>

            <input
              type="text"
              class="
                py-3
                block
                h-full
                flex-grow
                text-sm
                focus:outline-none
                text-[#626161]
                bg-[#e7e7e7]
              "
              placeholder="Find a restaurant"
            />

            <div
              class="
                px-5
                py-3
                flex
                items-center
                justify-center
                flex-grow-0
                text-[#626161]
              "
            >
              <MaterialIcon class="text-sm" icon="search" />
            </div>
          </div>
        </div>

        <div class="flex justify-end gap-3">
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
            Create Account
          </div>

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
            Login
          </div>
        </div>
      </div>
    </div>
    <Nuxt />
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>
