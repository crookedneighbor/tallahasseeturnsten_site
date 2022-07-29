<template>
  <div id="wrapper">
    <div id="logo-wrapper">
      <div>
        <img src="/album/tttlogo.png" alt="Tallahassee Turns Ten Logo" />
      </div>
    </div>

    <Separator />

    <BackgroundWash color="blue" class="flex align-center justify-center">
      <BackgroundWash
        color="black"
        class="border-white border-4 border-double text-white p-4 m-4 w-1/2"
      >
        <div>
          <h2 class="text-center text-5xl">About</h2>
          <p>
            On November 5th, 2002 The Mountain Goats released Tallahassee.
            Artists and fans across genres love John Darnielle's wordy, probing
            songs; and for many, Tallahassee was the album that made us fall in
            love. To celebrate its tenth birthday, Crooked Neighbor has
            commissioned fifteen bands to cover the album's fourteen songs (and
            one b-side), creating Tallahassee Turns Ten: A Mountain Goats Cover
            Album.
          </p>

          <p>
            The money from selling the compact disc version of the album went to
            supporting
            <NuxtLink to="https://www.farmsanctuary.org/" target="_blank"
              >Farm Sanctuary</NuxtLink
            >. You can download the record at
            <NuxtLink
              to="https://crookedneighbor.bandcamp.com/album/tallahassee-turns-ten"
              target="_blank"
              >Bandcamp</NuxtLink
            >.
          </p>
        </div>
        <div id="player">
          <iframe
            style="border: 0; width: 580px; max-width: 100%; height: 472px"
            class="m-auto"
            src="https://bandcamp.com/EmbeddedPlayer/album=1093339095/size=large/bgcol=ffffff/linkcol=e99708/artwork=none/transparent=true/"
            seamless
          ></iframe>
        </div>
      </BackgroundWash>
    </BackgroundWash>

    <div v-for="(song, index) in songs" :key="'song-id-' + index">
      <Separator />
      <Song
        :title="song.title"
        :artist="song.artist"
        :artist-link="song.artistLink"
        :participants="song.participants"
        :notes="song.notes"
        :track-number="index + 1"
        :background-color="song.backgroundColor"
      ></Song>
    </div>

    <Separator />
  </div>
</template>

<script lang="ts" setup>
const songs = [
  {
    title: "Tallahassee",
    artist: "Steve Slagg",
    artistLink: "https://steveslagg.com",
    backgroundColor: "red",
    participants: [
      {
        name: "Steve Slagg",
        credit: "Vocals, Prepared Piano",
      },
      {
        name: "Kerry J Haps",
        credit: "Piano Prep",
      },
    ],
    notes:
      "Recorded, mixed, and produced by Kerry J Haps of Hey, Darlin' Records at Archmart in the Shea Haps and Birchwood rooms. Wheaton, IL.",
  },
  {
    title: "First Few Desperate Hours",
    artist: "Your Heart Breaks",
    artistLink: "https://www.yourheartbreaks.com/",
    backgroundColor: "blue",
    participants: [
      {
        name: "Clyde Petersen",
        credit: "Keys and vocals",
      },
      {
        name: "Theo Hilton",
        credit: "Drums",
      },
      {
        name: "Jared Gandy",
        credit: "Bass",
      },
      {
        name: "Karl Blau",
        credit: "Sax and Vocals",
      },
    ],
    notes:
      "Produced by Your Heart Breaks. Recorded at Hot Soup Studios by Karl Blau in Anacortes, Wa",
  },
  {
    title: "Southwood Plantation Road",
    artist: "Mooner",
    artistLink: "https://moonerband.com/",
    backgroundColor: "yellow",
    participants: [
      {
        name: "Lee Ketch",
        credit: "vocals, electric guitar",
      },
      {
        name: "David Ketch",
        credit: "electric guitar",
      },
      {
        name: "Dann Morr",
        credit: "Bass",
      },
      {
        name: "Adam Bonich",
        credit: "drums",
      },
    ],
    notes:
      "Recorded, mixed, and produced by Kerry J Haps of Hey, Darlin' Records at Archmart in the Shea Haps and Birchwood rooms. Wheaton, IL.",
  },
  {
    title: "Game Shows Touch Our Lives",
    artist: "Kimya Dawson",
    artistLink: "http://kimyadawson.com/",
    backgroundColor: "purple",
    participants: [
      {
        name: "Kimya Dawson",
        credit: "vocals",
      },
      {
        name: "No One And The Somebodies",
        credit: "Arrangement",
      },
      {
        name: "Steve Yankou",
        credit: "guitar, cello",
      },
      {
        name: "Brian Yankou",
        credit: "drums",
      },
      {
        name: "Bobby Yankou",
        credit: "piano",
      },
      {
        name: "Kevin Yankou",
        credit: "deep throat hummer",
      },
      {
        name: "Jack Dishel (of Only Son)",
        credit: "1st guitar solo",
      },
      {
        name: "Jake Kelly",
        credit: "yodeling",
      },
    ],
    notes:
      "Engineered by Jake Kelly at Materials to Outlet Studio in Portland, Oregon.",
  },
  {
    title: "The House That Dripped Blood",
    artist: "Hallelujah the Hills",
    artistLink: "https://www.hallelujahthehills.com/",
    backgroundColor: "red",
    participants: [
      {
        name: "Ryan Walsh ",
        credit: "vocals, guitar",
      },
      {
        name: "Nicholas Giadone Ward ",
        credit: "bass, vocals",
      },
      {
        name: "Ryan Connelly",
        credit: "drums, vocals",
      },
      {
        name: "Brian Rutledge",
        credit: "trumpet",
      },
      {
        name: "David Bentley",
        credit: "cello",
      },
    ],
    notes: "Recorded, mixed and produced by Ryan Walsh.",
  },
  {
    title: "Idylls of the King",
    artist: "Miracles of Modern Science",
    artistLink: "https://www.miraclesofmodernscience.com/",
    backgroundColor: "purple",
    participants: [
      {
        name: "Evan Younger",
        credit: "vocals, double bass",
      },
      {
        name: "Josh Hirshfeld",
        credit: "mandolin",
      },
      {
        name: "Kieran Ledwidge",
        credit: "violin",
      },
      {
        name: "Geoff McDonald",
        credit: "cello",
      },
      {
        name: "Tyler Pines",
        credit: "drums",
      },
    ],
    notes:
      "Produced by Miracles of Modern Science. Recorded and mixed by Evan Younger in Brooklyn, NY.",
  },
  {
    title: "No Children",
    artist: "Laura Stevenson",
    artistLink: "https://www.laurastevenson.net/",
    backgroundColor: "white",
    participants: [
      {
        name: "Laura Stevenson",
        credit: "vocals, guitar, piano",
      },
    ],
    notes: "Recorded, mixed and produced by Laura Stevenson.",
  },
  {
    title: "See America Right",
    artist: "Jeffrey Lewis",
    artistLink: "http://www.thejeffreylewissite.com/",
    backgroundColor: "red",
    participants: [
      {
        name: "Jeffrey Lewis",
        credit: "vocals, guitar, drums",
      },
    ],
    notes: "Recorded, mixed and produced by Jeffrey Lewis.",
  },
  {
    title: "Peacocks",
    artist: "Houses",
    backgroundColor: "yellow",
    participants: [
      {
        name: "Dexter Tortoriello",
        credit: "Vocals, Synthesizers",
      },
      {
        name: "Megan Messina",
        credit: "Backing Vocals",
      },
    ],
    notes: "Produced by Houses. Recorded and mixed by Dexter Tortoriello.",
  },
  {
    title: "International Small Arms Traffic Blues",
    artist: "Tiger Waves",
    artistLink: "http://tigerwaves.bandcamp.com/",
    backgroundColor: "blue",
    participants: [
      {
        name: "Reid Comstock",
        credit: "vocals, guitar",
      },
      {
        name: "Joshua Kerl",
        credit: "drums, percussion",
      },
      {
        name: "James Marshall",
        credit: "guitar, vocals",
      },
      {
        name: "PJ Theberge",
        credit: "instruments, vocals",
      },
      {
        name: "Tyler Wharen",
        credit: "guitar, keys, vocals",
      },
    ],
    notes: "Produced by Tiger Waves.",
  },
  {
    title: "Have to Explode",
    artist: "Perry Owen Wright",
    backgroundColor: "purple",
    participants: [
      {
        name: "Perry Wright",
        credit: "vocals, guitars, bass, piano, rhodes, glockenspiel, mellotron",
      },
      {
        name: "Katie Spencer",
        credit: "background vocals",
      },
      {
        name: "Doug Campbell",
        credit: "background vocals",
      },
      {
        name: "Joshua Snyder",
        credit: "drums",
      },
      {
        name: "Scott Andrews",
        credit: "piano, rhodes, organ",
      },
      {
        name: "Shane McDonald",
        credit: "54321, ruby backend",
      },
    ],
    notes: "Recorded, mixed and produced by Perry Owen Wright.",
  },
  {
    title: "Old College Try",
    artist: "Mosaik featuring Saalik Ahmad Ziyad",
    artistLink: "https://kevinbrownguitar.com/",
    backgroundColor: "white",
    participants: [
      {
        name: "Saalik Ahmad Ziyad",
        credit: "vocals",
      },
      {
        name: "Andy Schlinder",
        credit: "tenor sax",
      },
      {
        name: "Kevin Brown",
        credit: "arrangement, fretless guitar",
      },
      {
        name: "Preyas Roy",
        credit: "Vibraphone",
      },
      {
        name: "Alex Wing",
        credit: "electric bass",
      },
      {
        name: "Nils Higdon",
        credit: "drums",
      },
    ],
    notes:
      "Produced by Mosaik. Recorded and Mixed by Caleb Willitz of Rattlesnake Studio, Chicago, IL.",
  },
  {
    title: "Oceanographer's Choice",
    artist: "Great Gray Buildings",
    backgroundColor: "yellow",
    participants: [
      {
        name: "Kevin Whelan",
        credit: "vocals, keyboard",
      },
      {
        name: "Matt Tanaka",
        credit: "drums",
      },
      {
        name: "Daniel Hawthorne",
        credit: "electric guitar",
      },
      {
        name: "Lee Ketch",
        credit: "bass",
      },
    ],
    notes:
      "Recorded, mixed, and produced by Kerry J Haps of Hey, Darlin' Records at Archmart in the Shea Haps and Birchwood rooms. Wheaton, IL.",
  },
  {
    title: "Alpha Rats Nest",
    artist: "AJJ",
    artistLink: "https://www.ajjtheband.com/",
    backgroundColor: "red",
    participants: [
      {
        name: "Sean Bonnette",
        credit: "vocals, guitar",
      },
      {
        name: "Ben Gallaty",
        credit: "bass, vocals",
      },
      {
        name: "Deacon Batchelor",
        credit: "drums",
      },
    ],
    notes:
      "Produced by Andrew Jackson Jihad. Recorded by jalipaz at audioconfusion.",
  },
  {
    title: "Ethiopians",
    artist: "Bomb the Music Industry!",
    artistLink: "https://bombthemusicindustry.tumblr.com/",
    backgroundColor: "blue",
    participants: [
      {
        name: "Mike Costa",
        credit: "drums",
      },
      {
        name: "John DeDomenici",
        credit: "bass",
      },
      {
        name: "Matt Keegan",
        credit: "guitars",
      },
      {
        name: "Tom Malinowski",
        credit: "guitars",
      },
      {
        name: "Jeff Rosenstock",
        credit: "guitars, vocals, harmonica, melodica & programming",
      },
    ],
    notes:
      "Produced by Bomb the Music Industry! Recorded by Tom Malinowski at Cellar Door Studios in Amityville, NY and Jeff Rosenstock at Quote Unquote Records in Brooklyn, NY. Mixed by Jeff Rosenstock.",
  },
];
</script>

<style scoped>
#logo-wrapper {
  background-image: url("/washes/redwash2.jpg");
  @apply flex justify-center p-4;
}

#logo-wrapper img {
  @apply max-w-full w-11/12;
}

#player {
  @apply p-4;
}

@media (min-width: 640px) {
  #logo-wrapper {
    background-image: url("/album/topartweb.jpg");
    @apply h-screen bg-cover bg-bottom;
  }
}
</style>
