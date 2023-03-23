<template>
  <div>
    <div class="hero-new short">
      <div class="wrap">
        <div class="breadcrumb-new">
          About Us <span class="circle"></span> Portfolio
        </div>
        <h1>We are true to our values</h1>
        <p>
          We work closely with our founders to understand their needs and goals,
          and we involve them in every step of the process, from ideation to
          execution. We take a partnership approach, working alongside our
          founders as a trusted and reliable resource.
        </p>
      </div>
    </div>
    <div class="manifest-wrap">
      <v-container>
        <v-row class="d-flex align-center">
          <v-col cols="12" sm="6" order-sm="2">
            <div
              class="circle-img"
              style="background-image: url('/Manifesto-Empower-Founder.png')"
            ></div>
          </v-col>
          <v-col cols="12" sm="6" order-sm="1">
            <h2>We <span class="bg-reds">empower</span> founders</h2>
            <p>
              We are founded by entrepreneurs, for entrepreneurs. We know what
              it takes to build a successful business, and we are dedicated to
              helping our founders achieve their visions. We take a hands-on
              approach, providing guidance, mentorship, and strategic support to
              help our founders overcome challenges and capitalize on
              opportunities.
            </p>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" sm="6">
            <div
              class="circle-img second"
              style="background-image: url('/Manifesto-Collaboration.png')"
            ></div>
          </v-col>
          <v-col cols="12" sm="6">
            <h2>We seek out <span class="bg-reds">collaboration</span></h2>
            <p>
              We believe in building strong and collaborative partnerships with
              our founders, working together as a team to achieve their goals.
              We take the time to get to know our founders and their unique
              needs, and we involve them in every step of the process, from
              initial ideation to final execution. We believe that open
              communication and collaboration is the key to success, and we are
              committed to building long-term relationships with our founders.
            </p>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" sm="6" order-sm="2">
            <div
              class="circle-img"
              style="background-image: url('/Manifesto-Great-Vision.png')"
            ></div>
          </v-col>
          <v-col cols="12" sm="6" order-sm="1">
            <h2>We focus on <span class="bg-reds">great vision</span></h2>
            <p>
              We take a long-term approach to venture building, focused on
              creating sustainable and successful businesses that will stand the
              test of time. We are not just interested in quick wins, but in
              building enduring companies that can make a real impact in the
              world. We believe that by taking a patient and strategic approach,
              we can create real value for our founders and investors alike.
            </p>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" sm="6">
            <div
              class="circle-img second"
              style="background-image: url('/Manifesto-Growth.png')"
            ></div>
          </v-col>
          <v-col cols="12" sm="6">
            <h2>We strive for <span class="bg-reds">growth</span></h2>
            <p>
              Our team brings a wealth of experience and network to the table,
              having successfully built and scaled multiple companies. We
              leverage this experience and network to help our founders overcome
              challenges, identify opportunities, and connect with the right
              people. We believe that the right network and experience can make
              all the difference in the success of a startup, and we are
              committed to sharing our knowledge and resources with our
              founders.
            </p>
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
    return {}
  },
  head() {
    return {
      title: 'Kolaborasi.co | Manifesto',
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
          content: 'Kolaborasi.co | Manifesto',
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
