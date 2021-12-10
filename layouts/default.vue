<template>
  <div class="min-h-screen">
    <div class="fixed top-0 left-0 z-10 w-full px-10 py-6 bg-white">
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
    <Nuxt />
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>
