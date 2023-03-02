<template>
  <div>
    <div class="service-head-new">
      <v-container>
        <v-row>
          <v-col cols="12" md="7">
            <div class="breadcrumb-new">
              Venture services <span class="circle"></span> {{ title }}
            </div>
            <h2 class="title-service">{{ slogan }}</h2>
            <p>
              {{ p1 }}
            </p>
            <p>
              {{ p2 }}
            </p>
            <p>Get the Solution Now</p>
            <img src="/phantom.png" alt="" />
          </v-col>
          <v-col cols="12" md="5">
            <div class="image-circle"></div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="service-business">
      <v-container>
        <v-row>
          <v-col cols="12">
            <h2 class="title-service text-center">
              Do these business challenges feel familiar to you?
            </h2>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="4">
            <div class="image-circle"></div>
          </v-col>
          <v-col cols="12" md="8">
            <div
              v-for="(item, index) in bItem"
              :key="index"
              class="business-item"
              :class="{ active: index === activeBusiness }"
              @click="setActive(index)"
            >
              <h4>{{ item.title }}</h4>
              <p>{{ item.desc }}</p>
            </div>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12">
            <h2 class="title-service text-center mt-16">Our Services</h2>
          </v-col>
          <v-col cols="4">
            <div class="service-item">
              <div class="image-circle"></div>
              <h6>Service 1</h6>
              <p>
                Any kind of design request for your Instagram needs, such as a
                single feed IG image, IG story, and carousel feed.
              </p>
            </div>
          </v-col>
          <v-col cols="4">
            <div class="service-item">
              <div class="image-circle"></div>
              <h6>Service 2</h6>
              <p>
                Any kind of design request for your Instagram needs, such as a
                single feed IG image, IG story, and carousel feed.
              </p>
            </div>
          </v-col>
          <v-col cols="4">
            <div class="service-item">
              <div class="image-circle"></div>
              <h6>Service 3</h6>
              <p>
                Any kind of design request for your Instagram needs, such as a
                single feed IG image, IG story, and carousel feed.
              </p>
            </div>
          </v-col>
          <v-col cols="4">
            <div class="service-item">
              <div class="image-circle"></div>
              <h6>Service 4</h6>
              <p>
                Any kind of design request for your Instagram needs, such as a
                single feed IG image, IG story, and carousel feed.
              </p>
            </div>
          </v-col>
          <v-col cols="4">
            <div class="service-item">
              <div class="image-circle"></div>
              <h6>Service 5</h6>
              <p>
                Any kind of design request for your Instagram needs, such as a
                single feed IG image, IG story, and carousel feed.
              </p>
            </div>
          </v-col>
          <v-col cols="4">
            <div class="service-item">
              <div class="image-circle"></div>
              <h6>Service 6</h6>
              <p>
                Any kind of design request for your Instagram needs, such as a
                single feed IG image, IG story, and carousel feed.
              </p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="subscribe">
      <v-container>
        <v-row>
          <v-col cols="12">
            <h2 class="title-service text-center black--text">
              Why Should You Subscribe to Us?
            </h2>
          </v-col>
          <v-col cols="12" md="6">
            <div class="subscribe-item">
              <div class="image-wrap"><img src="/subscribe1.png" alt="" /></div>
              <h5>Top Creative Talent</h5>
              <p>
                One-Stop Digital Product Design Solution, a leading digital
                product design partner to take your business to the next level
                of scale with ﬂexibility.
              </p>
            </div>
          </v-col>
          <v-col cols="12" md="6">
            <div class="subscribe-item">
              <div class="image-wrap"><img src="/subscribe2.png" alt="" /></div>
              <h5>24-48 hours turn-around time</h5>
              <p>
                One-Stop Digital Product Design Solution, a leading digital
                product design partner to take your business to the next level
                of scale with ﬂexibility.
              </p>
            </div>
          </v-col>
          <v-col cols="12" md="6">
            <div class="subscribe-item">
              <div class="image-wrap"><img src="/subscribe3.png" alt="" /></div>
              <h5>Hassle-free and reliable</h5>
              <p>
                One-Stop Digital Product Design Solution, a leading digital
                product design partner to take your business to the next level
                of scale with ﬂexibility.
              </p>
            </div>
          </v-col>
          <v-col cols="12" md="6">
            <div class="subscribe-item">
              <div class="image-wrap"><img src="/subscribe4.png" alt="" /></div>
              <h5>Wide variety of design capabilities</h5>
              <p>
                One-Stop Digital Product Design Solution, a leading digital
                product design partner to take your business to the next level
                of scale with ﬂexibility.
              </p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="price-new">
      <v-container>
        <v-row>
          <v-col cols="12">
            <h2 class="title-service text-center white--text">
              Pricing & Plans
            </h2>
            <p class="subtitle-service text-center">
              Choose any design pricing and plans suitable for your daily needs,
              from social media images to logo design.
            </p>
          </v-col>
          <v-col cols="12">
            <div class="price-wrap">
              <v-row>
                <v-col cols="3">
                  <div class="title no-border"></div>
                  <ul>
                    <li>Item 1</li>
                    <li>Item 2</li>
                    <li>Item 3</li>
                    <li>Item 4</li>
                    <li>Item 5</li>
                    <li>Item 6</li>
                    <li>Item 7</li>
                  </ul>
                </v-col>
                <v-col cols="3" class="border-left">
                  <div class="title"><h3>Basic Plan</h3></div>
                  <ul>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title"><h3>Premium Plan</h3></div>
                  <ul>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title"><h3>Bespoke Plan</h3></div>
                  <ul>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li>
                    <li><img src="/bcheck.png" alt="" /></li></ul
                ></v-col>
              </v-row>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="contact-new">
      <v-container>
        <v-row>
          <v-col md="5">
            <h3>Ready to take your business to another level?</h3>
            <a href=""><img src="/wa.png" alt="" /> Contact Us</a>
          </v-col>
        </v-row>
        <div class="image-wrap"></div>
      </v-container>
    </div>
    <div class="other-service">
      <v-container>
        <v-row>
          <v-col cols="10" offset="1">
            <h2 class="title-service text-center">
              Explore Our Other Services
            </h2>
            <a href=""><img src="/os1.png" alt="" /> Finance</a>
            <a href=""><img src="/os2.png" alt="" /> Marketing</a>
            <a href=""><img src="/os3.png" alt="" /> Human Resource</a>
            <a href=""><img src="/os4.png" alt="" /> Fundraising</a>
            <a href=""><img src="/os5.png" alt="" /> Legal</a>
            <a href=""><img src="/os6.png" alt="" /> Impact Management</a>
            <a href=""><img src="/os7.png" alt="" /> Community</a>
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
      title: '',
      slogan: '',
      p1: '',
      p2: '',
      bTitle: '',
      bItem: [],
      activeBusiness: 0,
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
        { hid: 'og:title', name: 'og:title', content: 'Kolaborasi.co' },
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
    if (this.$route.params.id === 'finance') {
      this.title = 'Finance'
      this.slogan = 'Boost your business decision accurately and conﬁdently'
      this.p1 =
        'Business decisions could be tough to make at times, how to ensure that every single of your decisions has the best impact on your business’ ﬁnancial condition and ultimately generate more proﬁt?'
      this.p2 =
        'With TMP, you can now conﬁdently grow your business with our highly reliable Financial Report that you can access 24/7 with high security, simple, and friendly to use.'
      this.bItem = [
        {
          title: 'Cash Flow Problems',
          desc: 'With TMP now you can keep your cash ﬂow in check by ensuring the perfect balance between your income and expenditures, therefore building a healthier ﬁnancial rapport.',
        },
        {
          title: 'Having an oversight about the real situation at hand',
          desc: 'With TMP now you can keep your cash ﬂow in check by ensuring the perfect balance between your income and expenditures, therefore building a healthier ﬁnancial rapport.',
        },
        {
          title: 'Tax reporting & compliance',
          desc: 'With TMP now you can keep your cash ﬂow in check by ensuring the perfect balance between your income and expenditures, therefore building a healthier ﬁnancial rapport.',
        },
      ]
    }
  },
  methods: {
    setActive(val) {
      this.activeBusiness = val
    },
  },
}
</script>
