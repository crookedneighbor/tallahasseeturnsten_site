<template>
  <BackgroundWash
    :color="backgroundColor"
    class="wrapper"
    :class="{ 'is-reversed': isReversed }"
  >
    <InfoBox
      :track-number="trackNumber"
      :title="title"
      :artist="artist"
      :artist-link="artistLink"
      :participants="participants"
      :notes="notes"
    />
    <div class="hidden sm:block my-4 z-50">
      <img
        :src="portraitPath"
        aria-hidden="true"
        class="m-auto max-h-screen"
        :class="{ 'md:-ml-8': !isReversed, 'md:-mr-8': isReversed }"
      />
    </div>
  </BackgroundWash>
</template>

<script lang="ts" setup>
const props = defineProps({
  trackNumber: {
    type: Number,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  artist: {
    type: String,
    required: true,
  },
  artistLink: {
    type: String,
    required: true,
  },
  participants: {
    type: Object,
    required: true,
  },
  notes: {
    type: String,
    required: true,
  },
  backgroundColor: {
    type: String,
    default: "red",
  },
});
const portraitPath = computed(() => {
  return `/portraits/${props.artist}.png`;
});
const isReversed = computed(() => {
  return props.trackNumber % 2 === 0;
});
</script>

<style scoped>
.wrapper {
  @apply p-4;
}

@media (min-width: 768px) {
  .wrapper {
    @apply h-screen flex justify-center items-center;
  }

  .wrapper.is-reversed {
    @apply flex-row-reverse;
  }
}
</style>
