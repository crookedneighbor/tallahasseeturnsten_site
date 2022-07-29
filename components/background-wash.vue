<template>
  <div :class="'wash-' + color"><slot /></div>
</template>

<script lang="ts" setup>
defineProps({
  color: {
    type: String,
    default: "red",
  },
});
</script>

<style scoped>
.wash-red {
  background-image: url("/washes/redwash.jpg");
}

.wash-blue {
  background-image: url("/washes/bluewash.jpg");
}

.wash-yellow {
  background-image: url("/washes/yellowwash.jpg");
}

.wash-purple {
  background-image: url("/washes/purplewash.jpg");
}

.wash-white {
  background-image: url("/washes/whitewash.jpg");
}

.wash-black {
  background-image: url("/washes/blackwash.jpg");
}
</style>
