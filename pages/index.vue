<template>
  <div id="wrapper">
    <div id="logo-wrapper">
      <div>
        <img src="/album/tttlogo.png" alt="Tallahassee Turns Ten Logo" />
      </div>
    </div>

    <Separator />

    <BackgroundWash color="blue" class="flex align-center justify-center">
      <BackgroundWash color="black" class="content-box">
        <div>
          <p class="mb-4">
            On November 5th, 2002 The Mountain Goats released Tallahassee.
            Artists and fans across genres love John Darnielle's wordy, probing
            songs; and for many, Tallahassee was the album that made us fall in
            love. To celebrate its tenth birthday, Crooked Neighbor has
            commissioned fifteen bands to cover the album's fourteen songs (and
            one b-side), creating Tallahassee Turns Ten: A Mountain Goats Cover
            Album.
          </p>

          <p class="my-4">
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

        <iframe
          style="border: 0; width: 580px; max-width: 100%; height: 472px"
          class="m-auto"
          src="https://bandcamp.com/EmbeddedPlayer/album=1093339095/size=large/bgcol=ffffff/linkcol=e99708/artwork=none/transparent=true/"
          seamless
        ></iframe>
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
    <BackgroundWash color="blue" class="flex align-center justify-center">
      <BackgroundWash color="black" class="content-box">
        <div>
          <h2 class="text-center text-5xl">Credits</h2>
          <p class="my-4">
            The record was produced by Crooked Neighbor LLC and Daniel Isaac
            Burrage. It was mastered by John McCaig at
            <NuxtLink to="http://www.panicstudios.com/" target="_blank"
              >Panic Studios</NuxtLink
            >. All artwork for the album and website was designed and rendered
            by
            <NuxtLink to="https://sarahgraley.com/" target="_blank"
              >Sarah Graley</NuxtLink
            >. All songs written by
            <NuxtLink To="https://www.mountain-goats.com/" target="_blank"
              >John Darnielle</NuxtLink
            >.
          </p>

          <p class="my-4">
            These wonderful people made this project possible by backing it on
            Kickstarter: Aaron Fraker, Abby Pullen, Adam Linder, Adam Sullivan,
            Alex Hughson, Alex Russell, Alex Wilgus, Alexandra,
            <NuxtLink to="http://allezallie.wordpress.com/" target="_blank"
              >Allison Meier</NuxtLink
            >, alpha_puppington, alyssa,
            <NuxtLink to="http://maybesproutwings.tumblr.com/" target="_blank"
              >Amanda Lucille</NuxtLink
            >, Andrew Kornfeld, andrewlips, Andy Gattis, Annmichelle, Ash
            Ponders,
            <NuxtLink to="http://deathlehem.tumblr.com/" target="_blank"
              >Aubri</NuxtLink
            >,
            <NuxtLink to="http://www.cllct.com/art/audleyspeeks" target="_blank"
              >Audley Speeks</NuxtLink
            >, Ben Zuerlein, Benjamin Silver, Binz, Brandon Lindquist, Brendan,
            Brian Clement, Brian Corstange, Caitlin Rose Boyle, Carla Arnold,
            Carly, Cassandra, Catherine Morris, Catherine Walsh,
            <NuxtLink to="http://www.cathyboy.com/" target="_blank"
              >Cathy G. Johnson</NuxtLink
            >, Celeste Adamson, charis,
            <NuxtLink to="http://charitykittler.com" target="_blank"
              >Charity Kittler</NuxtLink
            >, Chris Rediske, Christian Gridelli, Christopher MacMurray,
            <NuxtLink to="http://www.musicboomerang.com/" target="_blank"
              >"come trade your old CD's"</NuxtLink
            >, Corey Smith, Cory Banks, Craig Barringer, Crystal Baxley, Dallas
            Gentry, Dan Winkler, Daniel Albert, Daniel Barringer, Daniel Isaac
            Burrage, Daniel Godwin,
            <NuxtLink to="http://storiedtheology.com" target="_blank"
              >Daniel Kirk</NuxtLink
            >, Daniel Saunders, Daniela Isabella Ricci, Danielle Human Ross,
            Danny Martin, Derek Bosshard, Devon, Dianna Settles,
            <NuxtLink
              to="http://www.bloodygretagarbo.com/pasquinade"
              target="_blank"
              >Dominica Nicholls</NuxtLink
            >, Drew Thies, Dylan, Edward Goodson, Eibhlin McMenamin, Elaine,
            Elizabeth Tuck, Elliot Simmons,
            <NuxtLink to="http://twitter.com/Emily_Perper" target="_blank"
              >Emily Perper</NuxtLink
            >, Eric Brown, Eric Lowe, farynakita, Frank Fogarty,
            <NuxtLink to="http://jameater.cleanfolio.com" target="_blank"
              >Frankih Kay</NuxtLink
            >,
            <NuxtLink
              to="http://gabrielellisonricharde.bandcamp.com/"
              target="_blank"
              >Gabriel Ellison RiCharde</NuxtLink
            >, Grahm Eberhardt, Hansel, Heather O'Connor, Helena Ross, Huan
            Manton, Ian,
            <NuxtLink to="http://imathers.tumblr.com/" target="_blank"
              >Ian Mathers</NuxtLink
            >, Isaac Tyler, Isaac Valenzuela, Isobel, J, Jamie, Jathan Pugh,
            Jeff Killingsworth, Jeremiah White,
            <NuxtLink to="http://thelistcomic.com/" target="_blank"
              >Jerry Willoughby</NuxtLink
            >, john frewin, Johnathan Hansen, Jordan Michael Iannucci, Joseph
            Hatton, Joshua Huffman, Josiah Ostoich, Julia Ward,
            <NuxtLink to="http://volume-knob.blogspot.com/" target="_blank"
              >June Sezah Hatfield</NuxtLink
            >, Justin,
            <NuxtLink to="http://justindaley.bandcamp.com/" target="_blank"
              >Justin Mariner Daley</NuxtLink
            >, Kara Elliott-Ortega, Katelyn Leary, Kathryn Cullum, Kayleigh,
            Kevin, Kevin Seltzer, Kirsten Opstad, Kyle Auble, Kyle McKenna,
            <NuxtLink to="http://laurablumblr.tumblr.com/" target="_blank"
              >Laura Blum</NuxtLink
            >, Laura Cornwall, Laura Shapiro, Lauren, Lee Ogilvie, Leonard
            Richardson, Lewis Winter,
            <NuxtLink to="http://lastyearsgirl.pixlet.net" target="_blank"
              >Lis Ferla</NuxtLink
            >, Lola Smith, Louisa Amsterdam, Luke Brewster, Luke David Bather,
            <NuxtLink to="http://bliumchik.dreamwidth.org/" target="_blank"
              >Maggie K</NuxtLink
            >,
            <NuxtLink to="http://maiyaeats.tumblr.com/" target="_blank"
              >Maiya Wiester</NuxtLink
            >, mara, marc, Mariah Marconi, Mark Donaldson, Martin Atkinson,
            Marty Jones, Matthew Kuhmann,
            <NuxtLink
              to="http://thesoundandthefurry.tumblr.com/"
              target="_blank"
              >Matthew Monthei</NuxtLink
            >, max parmer, Max Smith, Megan Smith,
            <NuxtLink to="https://twitter.com/#!/kittenry" target="_blank"
              >Melvin Peña</NuxtLink
            >, Michael, Michael Kauffman, Michael OConnor, Michaela Drapes, Mike
            Dickison, Mikio, Monica Lynn Remmers, Nathaniel Remington Lovdahl,
            Nick Golding,
            <NuxtLink to="http://tampontears.tumblr.com/" target="_blank"
              >Nick Shulla</NuxtLink
            >, Nicole Bedard, Nigel Ewan, Nora Pullen, Omar Osegueda, Paulina
            Saba, Phil Brayshaw, Phoebe Rose Walker, Plutonium, Rachael Tucker,
            Rachel Thompson, Raishawn Wickwire, Rebecca Vitale, Rich Lawrence,
            Richard Fuss, Richie Manis,
            <NuxtLink
              to="http://kafka-on-the-road.blogspot.co.uk/"
              target="_blank"
              >Ryan O'Reilly</NuxtLink
            >, Ryan Steele, Sadie, Sal, Sam Bilheimer,
            <NuxtLink to="http://fatherthug.tumblr.com/" target="_blank"
              >Sam Logsdon</NuxtLink
            >, Sarah Avampato, Sarah Rattenborg,
            <NuxtLink
              to="http://www.flickr.com/photos/sashapedro"
              target="_blank"
              >Sasha Pedro</NuxtLink
            >, Siana Lacey, stacey noll, Stephen Tanksley, Steve and Tamara
            Hoey, Steve Keysor, Steven Smiley, Still Magiing, Suzanne Ditman,
            Tarasque Tymoshenko, Terry Herbert,
            <NuxtLink to="http://www.thewonderfullives.com/" target="_blank"
              >The Wonderful Lives</NuxtLink
            >,
            <NuxtLink to="https://twitter.com/itsthom" target="_blank"
              >Thom Ryan</NuxtLink
            >,
            <NuxtLink
              to="http://whatfreshheckisthis.tumblr.com/"
              target="_blank"
              >Tim Garvey</NuxtLink
            >, Timothy C. Gyves, to'c, Tom Pokorny, Tom Urwin, Tyler,
            <NuxtLink
              to="http://itunes.apple.com/us/podcast/ninjas-vs.-podcast/id473562353"
              target="_blank"
              >Tyler Crumrine</NuxtLink
            >,
            <NuxtLink to="http://twitter.com/valerie2776" target="_blank"
              >Valerie Barr</NuxtLink
            >, Walker Reynolds, Walt Evans, Walter Poulsen, Wyatt Hi-Hat Miller,
            xea-me,
            <NuxtLink to="http://www.twitter.com/zsghost" target="_blank"
              >Zach Gozlan</NuxtLink
            >, Zach Huselid
          </p>
        </div>
      </BackgroundWash>
    </BackgroundWash>

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

<style>
#logo-wrapper {
  background-image: url("/washes/redwash2.jpg");
  @apply flex justify-center p-8;
}

#logo-wrapper img {
  @apply max-w-full w-11/12;
}

.content-box {
  @apply border-white border-4 border-double text-white p-8 m-8 w-full lg:w-1/2;
}

a {
  @apply text-yellow-400;
}

@media (min-width: 640px) {
  #logo-wrapper {
    background-image: url("/album/topartweb.jpg");
    @apply h-screen bg-cover bg-bottom;
  }
}
</style>
