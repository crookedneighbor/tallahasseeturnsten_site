<template>
  <div id="wrapper">
    <div id="logo-wrapper">
      <img src="album/tttlogo.png" alt="Tallahassee Turns Ten Logo" />
    </div>

    <div id="nav-box">
      <iframe
        style="border: 0; width: 580px; max-width: 100%; height: 472px"
        class="m-auto"
        src="https://bandcamp.com/EmbeddedPlayer/album=1093339095/size=large/bgcol=ffffff/linkcol=e99708/artwork=none/transparent=true/"
        seamless
        ><a
          href="https://crookedneighbor.bandcamp.com/album/tallahassee-turns-ten"
          >Tallahassee Turns Ten by Crooked Neighbor</a
        ></iframe
      >
    </div>
  </div>
</template>

<style scoped>
#wrapper {
  background-image: url("washes/redwash2.jpg");
}

#logo-wrapper {
  @apply flex justify-center p-4;
}

#logo-wrapper img {
  @apply w-full max-w-3xl;
}

#nav-box {
  @apply p-4;
}

@media (min-width: 640px) {
  #wrapper {
    background-image: url("album/topartweb.jpg");
    @apply bg-cover bg-bottom;
  }
}
</style>
