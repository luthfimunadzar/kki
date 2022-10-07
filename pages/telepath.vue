<template>
  <div class="telepath">
    <div class="hero-wrap">
      <v-container>
        <v-row>
          <v-col md="12">
            <div class="types">
              <div class="top">
                <img src="/telepath.png" alt="" />
                <h4>shoots</h4>
              </div>
              <h2>{{ heros[0] }}</h2>
              <h3>messages to people’s minds.</h3>
            </div>
          </v-col>
        </v-row>
      </v-container>
      <img src="/pointer.png" alt="" class="pointer" />
      <img src="/thumb.png" alt="" class="thumb" />
      <img src="/eyes.png" alt="" class="eyes" />
      <img src="/rocket.png" alt="" class="rocket" />
    </div>
    <div class="concept">
      <v-container>
        <v-row>
          <v-col md="12">
            <p>
              we crunch high-level concepts into bite-size (and fun) contents
              such as:
            </p>
            <div class="text">
              <h3>Memes</h3>
              <img src="/meme.png" alt="" />
            </div>
            <div class="text text-right">
              <h3>Infographics</h3>
              <img src="/infog.png" alt="" />
            </div>
            <div class="text">
              <h3>Creative Contents</h3>
              <img src="/contents.png" alt="" />
            </div>
            <div class="text text-right">
              <h3>Motion Graphics</h3>
              <img src="/motion.png" alt="" />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="build">
      <v-container>
        <v-row>
          <v-col md="12">
            <h6>Or building them up into</h6>
            <div class="box">
              <h2>{{ builds[0] }}</h2>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="style">
      <img src="/telepath.png" alt="" class="logo" />
      <h4>Style // Identity // Philosophy</h4>
      <v-container>
        <v-row>
          <v-col cols="12" sm="4">
            <div class="style-warp">
              <img src="/style.png" alt="" />
              <h5>Clear, Concise, Clever</h5>
              <p>Fewer words, more meanings, plus a little spice</p>
            </div>
          </v-col>
          <v-col cols="12" sm="4">
            <div class="style-warp w-border">
              <img src="/philosophy.png" alt="" />
              <h5>Fun is never wrong</h5>
              <p>As long as they’re laughing with us.</p>
            </div>
          </v-col>
          <v-col cols="12" sm="4">
            <div class="style-warp w-border">
              <img src="/style.png" alt="" />
              <h5>Empathy through study</h5>
              <p>Know your audience, know who you are.</p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="work">
      <h4>Our Collective Works</h4>
      <div class="d-block text-center">
        <a
          v-for="work in works"
          :key="work.id"
          :href="work.link"
          target="_blank"
          class="work-warp"
          :style="{ backgroundImage: `url(${work.img})` }"
        >
          <span>{{ work.title }}</span>
          <div class="overlay">{{ work.title }}</div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'blank',
  data() {
    return {
      works: [
        {
          id: 1,
          img: '/works1.png',
          title: 'Cityplan',
          link: 'https://www.instagram.com/cityplan.id/?igshid=YmMyMTA2M2Y%3D',
        },
        {
          id: 2,
          img: '/works2.png',
          title: 'Kolaborasi',
          link: 'https://www.instagram.com/kolaborasico/?igshid=YmMyMTA2M2Y%3D',
        },
        {
          id: 3,
          img: '/works3.png',
          title: 'Lexar',
          link: 'https://docs.google.com/presentation/d/15LclhLKmsCRj7qvF0f8a1MaolklbvqidY3_md2aMCaE/edit#slide=id.g161154a7003_0_111',
        },
        {
          id: 4,
          img: '/works4.png',
          title: 'SIAP',
          link: 'https://instagram.com/socialinnovation.id?igshid=YmMyMTA2M2Y=',
        },
        {
          id: 5,
          img: '/works5.png',
          title: 'MGEE',
          link: '/mgee.pdf',
        },
      ],
      builds: ['Brand Book', 'Campaign', 'Visual Activation'],
      heros: [
        'enthralling',
        'exciting',
        'funny',
        'memorable',
        'dramatic',
        'lovely',
        'digestible',
        'playful',
        'trustworthy',
      ],
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Telepath',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
        {
          hid: 'og:title',
          name: 'og:title',
          content: 'Kolaborasi.co | Telepath',
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
  mounted() {
    window.setInterval(() => {
      this.changeBuild()
    }, 3000)
    window.setInterval(() => {
      this.changeHeros()
    }, 1000)
  },
  methods: {
    changeBuild() {
      const first = this.builds.shift()
      this.builds = this.builds.concat(first)
    },
    changeHeros() {
      const first = this.heros.shift()
      this.heros = this.heros.concat(first)
    },
  },
}
</script>
