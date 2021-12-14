<template>
  <div class="border rounded-xl px-4 py-3 shadow bg-white/60">
    <div class="">
      <p class="text-base font-bold">{{ template.name }}</p>
      <p class="text-xs">
        {{ template.description }}
      </p>
    </div>

    <div class="mt-4">
      <div v-if="type === 'rating'" class="flex flex-col gap-2">
        <div
          v-for="field in template.fields"
          :key="field.name"
          class="flex items-center"
        >
          <div class="w-2/5">
            <p class="text-sm font-bold leading-none">{{ field.name }}</p>
          </div>
          <div class="flex-grow">
            <StarRating size="lg" :count="false" :tight="false" />
          </div>
        </div>
      </div>

      <div v-else-if="type === 'textarea'" class="">
        <textarea
          class="
            border
            rounded-xl
            text-sm
            px-4
            py-3
            focus:outline-none
            bg-transparent
            w-full
          "
          cols="30"
          rows="10"
          :placeholder="placeholder"
        ></textarea>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AStarReviewCard',

  props: {
    type: {
      type: String,
      default: 'rating',
    },

    placeholder: {
      type: String,
      default: 'Text here',
    },

    template: {
      type: Object,
      required: true,
    },
  },
}
</script>
