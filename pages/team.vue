<template>
  <div>
    <div class="hero-new short">
      <div class="wrap">
        <div class="breadcrumb-new">
          About Us <span class="circle"></span> Team
        </div>
        <h1>Co-founders & Partners</h1>
        <p>
          Leverage agile frameworks to provide a robust synopsis for high level
          overviews. Iterative approaches to corporate strategy foster
          collaborative thinking to further the overall value proposition.
          achieve a common goal.
        </p>
      </div>
    </div>
    <div class="team-wrap">
      <v-container>
        <v-row class="d-flex justify-center">
          <v-col
            v-for="(team, index) in founders"
            :key="team.id"
            cols="12"
            sm="6"
            md="4"
          >
            <div
              class="team-item"
              :class="[
                { second: index === 1 },
                { third: index === 2 },
                { four: index === 3 },
                { five: index === 4 },
              ]"
            >
              <div
                class="image"
                :style="{ backgroundImage: `url(${team.img})` }"
              ></div>
              <div class="text">
                <h3>{{ team.name }}</h3>
                <p>{{ team.desc }}</p>
                <a :href="team.linkedin" class="socmed">
                  <v-icon> fab fa-linkedin </v-icon>
                </a>
                <a :href="team.ig" class="socmed">
                  <v-icon> fab fa-instagram </v-icon>
                </a>
                <a :href="team.twitter" class="socmed">
                  <v-icon> fab fa-twitter </v-icon>
                </a>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'new',
  data() {
    return {
      founders: [
        {
          id: 1,
          img: '/Consult-Now-HR.png',
          name: 'Adryan Haﬁzh',
          desc: 'Expertise ranging from product development, innovation management, leadership, to multiple roles in mobile legend. Energetic but loving, Pushing but protecting, Innovative but wise. Adryan is the man with many solutions.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 2,
          img: '/Consult-Now-Finance.png',
          name: 'Aldi Ulaan',
          desc: 'Expertise ranging from financial strategy, business administration, to Underground Asian pop-culture. Joyous but governing, organized but playful, modest but infectiously positive. Ulaan is the man behind most guns.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 3,
          img: '/Consult-Now-Content_Design.png',
          name: 'Sutansyah Marahakim',
          desc: 'Expertise ranging from copywriting, branding, to action figure collecting. Aggressive but fun-loving, practical but philosophical, sharp but charismatic. Sutan is the creative force of the team.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 4,
          img: '/Consult-Now-Impact.png',
          name: 'Moon Marva',
          desc: 'Expertise ranging from marketing, organisational management, to manga connoisseur. Calm but enthused, systematic but explorative, polite but decisive. Moon is the neat mother with a nerd soul.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 5,
          img: '/Consult-Fundraising.png',
          name: 'Aldi Adrian',
          desc: 'Expertise ranging from corporate strategy, fundraising, to professional Netflix clickers. Thorough but casual, analytical but charming, critical but knowledgeable. Al is the trailblazer to our next step.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Team',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
        {
          hid: 'og:title',
          name: 'og:title',
          content: 'Kolaborasi.co | Team',
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content:
            'kolaborasi, kolaborasi kapital indonesia, startup, incubator',
        },
        {
          hid: 'og:description',
          name: 'og:description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
      ],
    }
  },
  methods: {},
}
</script>
