<template>
  <div class="flex items-center">
    <div class="flex items-center mr-1 text-brand-yellow">
      <MaterialIcon icon="star" :class="[starSize]" />
      <MaterialIcon icon="star" :class="[starSize]" />
      <MaterialIcon icon="star" :class="[starSize]" />
      <MaterialIcon icon="star_half" :class="[starSize]" />
      <MaterialIcon icon="star_outline" :class="[starSize]" />
    </div>
    <span
      v-if="count"
      class="text-[10px] text-brand-gray leading-snug tracking-tight"
      >2.4k</span
    >
  </div>
</template>

<script>
export default {
  name: 'StarRatings',

  props: {
    count: {
      type: Boolean,
      default: true,
    },

    size: {
      type: String,
      default: null,
    },
  },

  computed: {
    starSize() {
      let size = null
      switch (this.size) {
        case 'md':
          size = 'text-base'
          break

        default:
          size = 'text-xs'
          break
      }

      return size
    },
  },
}
</script>
