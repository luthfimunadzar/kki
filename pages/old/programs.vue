<template>
  <div>
    <div class="programs-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1">
            <h3>Hyper Founder Programs</h3>
            <v-row align="center">
              <v-col cols="12" sm="6" class="text-center">
                <img src="/what-we-do.png" alt="" class="max-width" />
              </v-col>
              <v-col cols="12" sm="6">
                <h5>A. What we Do</h5>
                <p>
                  Hyper Founder Program is a venture building program where we
                  support your early stage business within the function of
                  “Product Development / Team & Work Management / Go to Market
                  Strategy. We act as a “venture partner” which is a combination
                  of “coworker + mentor + coach + manager” that work hands-on
                  with you to get things done.
                </p>
              </v-col>
            </v-row>
            <v-row class="mt-10" align="center">
              <v-col cols="12" sm="6" class="text-center order-sm-second">
                <img src="/what-will-you-get.png" alt="" class="max-width" />
              </v-col>
              <v-col cols="12" sm="6" class="order-sm-first">
                <h5 class="text-sm-right">B. What will you get?</h5>
                <p class="text-sm-right">
                  You will get a dedicated working partner, working with the
                  agreed time frame, who will work side by side with you & your
                  team from planning, managing, and executing the activity
                  needed to reach the target milestone. You will get the best
                  practice, network, and framework that gathered in our 8+ year
                  experiences of building an early stage business in various
                  industries.
                </p>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12">
                <div class="text-center">
                  <nuxt-link
                    to="/hyperhunt"
                    class="btn btn-primary d-inline-block red"
                    ><span>Apply Now</span>
                  </nuxt-link>
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>

    <div class="program-wrap pt-0">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Lab Services</h3>
            <v-row>
              <v-col md="4" sm="6" cols="12">
                <div class="item-service second">
                  <h5>Telepath</h5>
                  <p>
                    We will act as your digital marketing manager which covers
                    content strategy, graphic design, campaigns, and digital
                    advertising.
                  </p>
                  <nuxt-link
                    to="/contact"
                    class="btn btn-primary d-inline-block red"
                    ><span>Contact Us</span>
                  </nuxt-link>
                  <img src="/service-1.png" alt="" />
                </div>
              </v-col>
              <v-col md="4" sm="6" cols="12">
                <div class="item-service">
                  <h5>Phantom</h5>
                  <p>
                    We will act as your CFO which covers regular bookkeeping,
                    taxation, legal documentation, and initial hiring process at
                    a fraction of the cost.
                  </p>
                  <nuxt-link
                    to="/contact"
                    class="btn btn-primary d-inline-block red"
                    ><span>Contact Us</span>
                  </nuxt-link>
                  <img src="/service-2.png" alt="" />
                </div>
              </v-col>
              <v-col md="4" sm="12" cols="12">
                <v-row>
                  <v-col md="12" sm="6" cols="12" class="pb-md-0">
                    <div class="item-service third h50">
                      <h5>Metamorph</h5>
                      <a href="#">Coming Soon</a>
                      <img src="/service-3.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="12" sm="6" cols="12" class="pt-md-0">
                    <div class="item-service four h50">
                      <h5>Levitate</h5>
                      <a href="#">Coming Soon</a>
                      <img src="/service-4.png" alt="" />
                    </div>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>

    <div class="faq-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12">
            <h4 class="text-center faq-title">FAQ</h4>
            <v-expansion-panels accordion light>
              <v-expansion-panel v-for="(item, i) in faqs" :key="i">
                <v-expansion-panel-header>
                  <vue-markdown :source="item.question" />
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  <vue-markdown :source="item.answer" />
                </v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
import VueMarkdown from 'vue-markdown'
export default {
  components: {
    VueMarkdown,
  },
  data() {
    return {
      founders: [
        {
          id: 1,
          img: '/people1.png',
          name: 'John Doe',
          desc: 'John Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 2,
          img: '/people2.png',
          name: 'John Doe',
          desc: 'John Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 3,
          img: '/people3.png',
          name: 'Jane Doe',
          desc: 'Jane Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 4,
          img: '/people4.png',
          name: 'Jane Doe',
          desc: 'Jane Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
      ],
      familys: [
        {
          id: 1,
          img: '/partner1.png',
          name: 'Crowde',
          desc: 'Revolutionise agriculture industry through financial & agri-tech innovation',
          link: 'https://crowde.co/',
        },
        {
          id: 2,
          img: '/partner2.png',
          name: 'Lingkaran',
          desc: 'Bridging gap between formal education & industry through alternative education & digital content',
          link: 'http://lingkaran.co/',
        },
        {
          id: 3,
          img: '/partner3.png',
          name: 'City Plan',
          desc: 'Supporting govt & industry build a better cities through spatial data intelligence solutions',
          link: 'http://cityplan.id/',
        },
        {
          id: 4,
          img: '/partner4.png',
          name: 'Brocode Barber',
          desc: 'Bringing a new standard of customer service in a chain of barbershop',
          link: 'https://www.brocodebarber.com/',
        },
        {
          id: 5,
          img: '/partner5.png',
          name: 'Robonesia',
          desc: 'A robotic education program for elementary students',
          link: 'http://robonesia.id/',
        },
        {
          id: 6,
          img: '/partner6.png',
          name: 'Freenovation',
          desc: 'Redefining the future of work through coworking movement',
          link: 'http://freenovation.co/',
        },
      ],
      builders: [
        {
          id: 1,
          img: '/partner7.png',
          name: 'Smile Concept',
          desc: 'A customer focused dental clinic that not only treat but educate people about oral health',
          link: 'https://smileconceptclinic.com/',
        },
        {
          id: 2,
          img: '/partner8.png',
          name: 'Freelens Studio',
          desc: 'Capturing moment & conveying message through video solution',
          link: 'http://freelens.id/',
        },
        {
          id: 3,
          img: '/partner9.png',
          name: 'Lexar',
          desc: 'Simplifying legal & corporate secretarial process for SME with tailored service & digital product',
          link: 'http://lexar.id/',
        },
      ],
      siaps: [
        {
          id: 1,
          img: '/partner10.png',
          name: 'Menjadi Manusia',
          desc: 'Social platform to share the alternative perspective in the form of video content & activation',
          link: 'https://www.youtube.com/channel/UCJ6JnLmidOIP1sFeK8hRspA',
        },
        {
          id: 2,
          img: '/partner11.png',
          name: 'Berdaya Krui',
          desc: 'Building an impactful & sustainable tourism initiatives to empower local economy',
          link: 'http://berdaya.co/',
        },
        {
          id: 3,
          img: '/partner12.png',
          name: 'SaveYourselves',
          desc: 'Building platform to help people with mental health issues',
          link: 'http://saveyourselves.id/',
        },
        {
          id: 4,
          img: '/partner13.png',
          name: 'Baca PiBo',
          desc: 'Creating digital pictured book library for toddler',
          link: 'https://www.bacapibo.com/index.html',
        },
      ],
      faqs: [
        {
          id: 1,
          question:
            '<em>1. What is the difference between “Hyper Founder Program” and “Lab Service”?</em>',
          answer:
            '<ol style="list-style-type: lower-alpha;"><li>Hyper Founder Program is a venture building program where we support your business within the function of “Product Development / Team & Work System / Go to Market Strategy. We act as a <b>“venture partner”</b> which is a combination of “coworker + mentor + coach + manager” that work hands-on with you to get things done.</li><li>Our Phantom & Telepath is an <b>agency</b> that will provide professional service tailored to the needs of your startup. We provide an affordable monthly subscription with a minimum contract of 3 month.</li></ol>',
        },
        {
          id: 2,
          question:
            '<em>2. Is the “Hyper Founder Program” an incubator or accelerator?</em>',
          answer:
            '<ol style="list-style-type: lower-alpha;"><li>NO we are not an incubator or accelerator that provides a typical series of workshops for 3-4 months, gives you free office, free credits of AWS, runs a demo day for you, and after all the press coverage is released, the program is done.  No, we dont do that here</li><li>What we ARE, is a personalised venture builder where there will be 1-2 people from our team who will be assigned to be your “Capo” (unique combination of coworker + mentor + coach + manager). Together, we will discuss, plan and execute with agreed tasks & deliverables as an internal team.</li></ol>',
        },
        {
          id: 3,
          question:
            '<em>3. Do we need to pay for Hyper Founder or Lab Service?</em>',
          answer:
            '<ol style="list-style-type: lower-alpha;"><li>For the Hyper Founder program, we will provide a “free trial service” for the first 3 months. If both parties agree, we might continue the service by taking up to 15% of sweat equity, for a lifetime commitment of working together with you.</li><li>For Phantom & Telepath, yes we charge a monthly subscription for the service with the minimum contract of 3 months. For Phantom, start at RpXXX, for Telepath, start at RpYYY. Which is very worth your money for what you will get from us!</li></ol>',
        },
        {
          id: 4,
          question:
            '<em>4. What’s the criteria of a startup / founder that can apply to Hyper Founder & Lab Service?</em>',
          answer:
            '<ol style="list-style-type: lower-alpha;"><li>For the Hyper Founder program, we are sector agnostic (we accept almost all industries, from tech startup, creative business, agriculture, commodity, lifestyle, etc) . In terms of the stage, we are expecting at least you have a working prototype + prior knowledge & experience in the field.</li><li>Nope, as long as you have money to get a good quality service for a very good price</li></ol>',
        },
        {
          id: 5,
          question: '<em>5. How do I apply? When can I apply?</em>',
          answer:
            '<ol style="list-style-type: lower-alpha;"><li>For the HYPER Founder Program, we will start the “pre-intake assessment” from August. The selection and pre-program will run until December. Then the chosen Founder will officially “join the family” and start the journey together with us, in January 2022. Kindly fill the FORM (link) to get started</li><li>For Phantom & Telepath, you can fill in the FORM (link) to get started. Then our team will contact you ASAP.</li></ol>',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Programs & Services',
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
          content: 'Kolaborasi.co | Programs & Services',
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
