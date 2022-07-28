<template>
  <div id="wrapper">
    <div id="logo-wrapper">
      <img src="public/album/tttlogo.png" alt="Tallahassee Turns Ten Logo" />
    </div>

    <div id="nav-box">
      <iframe
        style="border: 0; width: 580px; max-width: 100%; height: 472px"
        class="m-auto"
        src="https://bandcamp.com/EmbeddedPlayer/album=1093339095/size=large/bgcol=ffffff/linkcol=e99708/artwork=none/transparent=true/"
        seamless
      ></iframe>
    </div>
  </div>
</template>

<style scoped>
#wrapper {
  background-image: url("public/washes/redwash2.jpg");
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
    background-image: url("public/album/topartweb.jpg");
    @apply bg-cover bg-bottom;
  }
}
</style>
