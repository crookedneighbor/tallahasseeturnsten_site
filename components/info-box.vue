<template>
  <BackgroundWash color="black" class="info-box">
    <div class="main-info">
      <div class="track-number" aria-hidden>{{ track }}</div>
      <div>{{ title }}</div>
      <div class="text-2xl">
        by
        <NuxtLink v-if="artistLink" :to="artistLink" target="_blank">{{
          artist
        }}</NuxtLink>
        <span v-else>{{ artist }}</span>
      </div>
    </div>

    <div class="credit-info">
      <div
        v-for="participant of participants"
        :key="trackNumber + '-' + participant.name"
      >
        <span class="font-bold">{{ participant.name }}</span
        >&nbsp;
        <span class="text-gray-300">{{ participant.credit }}</span>
      </div>
      <hr class="my-2 border-gray-400" />
      <div class="text-gray-300">{{ notes }}</div>
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
    default: "",
  },
  participants: {
    type: Object,
    required: true,
  },
  notes: {
    type: String,
    required: true,
  },
});
const track = computed(() => {
  if (props.trackNumber < 10) {
    return `0${props.trackNumber}`;
  }

  return String(props.trackNumber);
});
</script>

<style scoped>
.info-box {
  @apply z-0 m-auto relative text-white border-white border-4 border-double p-4 max-w-full w-96 h-min;
}

.main-info {
  font-family: Optima, Tahoma, sans-serif;
  @apply text-center text-4xl mb-4;
}

.credit-info {
  @apply text-sm;
}

.track-number {
  @apply text-gray-400;
}

@media (min-width: 768px) {
  .info-box {
    @apply m-0;
  }
  .track-number {
    @apply absolute top-1 right-2;
  }

  .main-info {
    @apply mt-6;
  }
}
</style>
