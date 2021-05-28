<template>
  <div>
    <div v-if="!quiz" class="hero">
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1" class="position-relative">
            <h2>
              We help founders build their dream through venture building
              program
            </h2>
            <a class="go-quiz" @click="showQuiz()">
              <p>Do you have what it takes to be a HYPER Founder?</p>
              <span>Start</span>
            </a>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div v-if="quiz" class="quiz">
      <div
        v-for="(item, index) in question"
        :key="item.id"
        :class="['item-quiz', { 'd-none': hiddenQestion[index] === 'hide' }]"
      >
        <h3>
          <span>{{ item.quiz }}</span>
        </h3>
        <a
          :class="['step', 'left', { active: answer[index] === 'a' }]"
          @click="pickQuiz(index, 'a')"
        >
          <div class="wrap">
            <h4>{{ item.answer_a }}</h4>
            <div class="clearfix"></div>
            <span class="circle"></span>
          </div>
        </a>
        <a
          :class="['step', 'right', { active: answer[index] === 'b' }]"
          @click="pickQuiz(index, 'b')"
        >
          <div class="wrap">
            <h4>{{ item.answer_b }}</h4>
            <div class="clearfix"></div>
            <span class="circle"></span>
          </div>
        </a>
        <a v-if="hiddenQestion[0]" class="prev" @click="quizBack(index)">
          <v-icon> fas fa-angle-left </v-icon> Previous question</a
        >
        <p class="count">Question {{ index + 1 }}/{{ question.length }}</p>
      </div>
      <div v-if="result" class="result">
        <div class="result-wrap">
          <div class="wrap">
            <h5>Congrats! You are a...</h5>
            <h2>HYPER FOUNDER!</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut
              finibus mattis turpis, at tempus justo malesuada in.
            </p>
            <p>
              Sed ante lectus, fermentum id elit et, convallis lacinia purus.
              Aliquam erat volutpat. Vivamus ultrices diam in lorem sodales, a
              placerat enim suscipit.
            </p>
            <a class="link-retake" @click="resetTest()">RETAKE THE TEST</a>
            <div class="clearfix"></div>
            <a href="" class="btn btn-primary btn-more"
              ><span>See what KOLABORASI can do for you</span></a
            >
          </div>
        </div>
      </div>
    </div>
    <div class="hyper-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12">
            <h3>What is HYPER Founder?</h3>
            <v-tabs v-model="tab" align-with-title>
              <v-tab v-for="item in tabItems" :key="item">
                {{ item }}
              </v-tab>
            </v-tabs>

            <v-tabs-items v-model="tab">
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5>HELPFUL</h5>
                    <p>
                      Specialists in this rapidly evolving industry, we have an
                      innate understanding of the media sector because we choose
                      to immerse ourselves in it. Our team is actively involved
                      in the media industry and are board members of, or
                      advisors to, various industry organisations: Women in Film
                      and Television, NZ Tech Industry Association and the NZ
                      Game Developers Association.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="blue">YLPFUL</h5>
                    <p>
                      Specialists in this rapidly evolving industry, we have an
                      innate understanding of the media sector because we choose
                      to immerse ourselves in it. Our team is actively involved
                      in the media industry and are board members of, or
                      advisors to, various industry organisations: Women in Film
                      and Television, NZ Tech Industry Association and the NZ
                      Game Developers Association.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="cyan">PFUL</h5>
                    <p>
                      Specialists in this rapidly evolving industry, we have an
                      innate understanding of the media sector because we choose
                      to immerse ourselves in it. Our team is actively involved
                      in the media industry and are board members of, or
                      advisors to, various industry organisations: Women in Film
                      and Television, NZ Tech Industry Association and the NZ
                      Game Developers Association.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="yellow">EFUL</h5>
                    <p>
                      Specialists in this rapidly evolving industry, we have an
                      innate understanding of the media sector because we choose
                      to immerse ourselves in it. Our team is actively involved
                      in the media industry and are board members of, or
                      advisors to, various industry organisations: Women in Film
                      and Television, NZ Tech Industry Association and the NZ
                      Game Developers Association.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="green">REFUL</h5>
                    <p>
                      Specialists in this rapidly evolving industry, we have an
                      innate understanding of the media sector because we choose
                      to immerse ourselves in it. Our team is actively involved
                      in the media industry and are board members of, or
                      advisors to, various industry organisations: Women in Film
                      and Television, NZ Tech Industry Association and the NZ
                      Game Developers Association.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
            </v-tabs-items>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="founder-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Our HYPER Founders</h3>
            <v-carousel :show-arrows="false">
              <v-carousel-item v-for="item in founders" :key="item.id">
                <h4>{{ item.name }}</h4>
                <p>{{ item.desc }}</p>
                <a>Founders Proﬁle</a>
                <div class="clearfix"></div>
                <img :src="item.img" alt="" />
              </v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="program-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Programs & Services</h3>
            <v-row>
              <v-col sm="6" cols="12">
                <div class="item-programs">
                  <h4>What we do</h4>
                  <img src="/what-we-do.png" alt="" />
                  <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam
                    consectetur dolor in lacinia placerat. In id cursus lorem.
                  </p>
                </div>
              </v-col>
              <v-col sm="6" cols="12">
                <div class="item-programs w-border">
                  <h4>What will you get</h4>
                  <img src="/what-will-you-get.png" alt="" />
                  <p>
                    Nam eu dui dapibus, finibus felis quis, malesuada libero.
                    Curabitur tempus enim suscipit sagittis rutrum.
                  </p>
                </div>
              </v-col>
              <v-col cols="12">
                <h4 class="text-center">Our Services</h4>
                <v-row>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service">
                      <h5>Pitch Deck Making</h5>
                      <img src="/service-1.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service second">
                      <h5>Content Marketing & Wordsmithing</h5>
                      <img src="/service-2.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service third">
                      <h5>Financial Planning & Structuring</h5>
                      <img src="/service-3.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service four">
                      <h5>Graphic Design</h5>
                      <img src="/service-4.png" alt="" />
                    </div>
                  </v-col>
                </v-row>
                <div class="text-center mt-8">
                  <a class="btn btn-primary d-inline-block red"
                    ><span>All Programs & Services</span></a
                  >
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="contact-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Contact Us</h3>
            <v-row>
              <v-col cols="12" md="6">
                <h5>Our Home Base</h5>
                <p>
                  Komplek Kampung Padi B11<br />
                  Dago Pojok, Bandung<br />
                  West Java, Indonesia<br />
                  40132
                </p>
                <h5>For Fast Response</h5>
                <a href="mailto:contact@kolaborasi.co"
                  ><v-icon>far fa-envelope</v-icon> contact@kolaborasi.co</a
                >
                <div class="clearfix"></div>
                <a href="http://wa.link/pmub9a"
                  ><v-icon>fab fa-whatsapp</v-icon> 0818 0944 2483</a
                >
              </v-col>
              <v-col cols="12" md="6">
                <h5>Send Us a Message</h5>
                <validation-observer ref="observer">
                  <form @submit.prevent="submit">
                    <validation-provider
                      v-slot="{ errors }"
                      name="Your Name"
                      rules="required"
                    >
                      <v-text-field
                        v-model="form.name"
                        :error-messages="errors"
                        label="Your Name"
                        required
                      ></v-text-field>
                    </validation-provider>
                    <validation-provider
                      v-slot="{ errors }"
                      name="Your Email"
                      rules="required|email"
                    >
                      <v-text-field
                        v-model="form.email"
                        :error-messages="errors"
                        label="Your E-mail"
                        required
                      ></v-text-field>
                    </validation-provider>
                    <validation-provider
                      v-slot="{ errors }"
                      name="Your Message"
                      rules="required"
                    >
                      <v-textarea
                        v-model="form.message"
                        :error-messages="errors"
                        label="Your Message"
                        required
                        auto-grow
                      ></v-textarea>
                    </validation-provider>
                    <button class="btn btn-primary yellow mt-5" type="submit">
                      <span>Send Message</span>
                    </button>
                  </form>
                </validation-observer>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'

export default {
  data() {
    return {
      form: {
        name: null,
        email: null,
        message: null,
      },
      result: false,
      quiz: false,
      tab: null,
      tabItems: ['H', 'Y', 'P', 'E', 'R'],
      answer: [],
      hiddenQestion: [],
      question: [
        {
          id: 1,
          quiz: 'How much risk do you like to take in life?',
          answer_a: 'As little as possible',
          answer_b: 'I get a buzz from taking crazy risks all the time',
        },
        {
          id: 2,
          quiz: 'Nam eget ornare mauris. In ultrices augue ac leo semper?',
          answer_a: 'vel ultricies eros cursus',
          answer_b: 'Sed non mauris vel velit aliquam',
        },
        {
          id: 3,
          quiz: 'bibendum velit at, placerat mauris?',
          answer_a: 'porttitor eget at felis',
          answer_b: 'Sed ut odio volutpat',
        },
        {
          id: 4,
          quiz: 'Pellentesque iaculis, risus sed mollis tempor?',
          answer_a: 'sapien massa auctor erat',
          answer_b: 'a eleifend tellus odio',
        },
      ],
      founders: [
        {
          id: 1,
          img: '/people.png',
          name: 'John Doe Long Name',
          desc: 'John Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise, surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
        },
        {
          id: 2,
          img: '/people.png',
          name: 'Jean Doe Long Name',
          desc: 'Jean Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise, surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
        },
        {
          id: 3,
          img: '/people.png',
          name: 'Jean Doe Long Name',
          desc: 'Jean Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise, surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
        },
      ],
    }
  },
  methods: {
    pickQuiz(index, value) {
      Vue.set(this.answer, index, value)
      setTimeout(() => {
        Vue.set(this.hiddenQestion, index, 'hide')
        if (this.hiddenQestion[this.question.length - 1] === 'hide') {
          this.result = true
        }
      }, 1000)
    },
    resetTest() {
      this.answer = []
      this.hiddenQestion = []
      this.result = false
    },
    quizBack(index) {
      Vue.set(this.hiddenQestion, index - 1, null)
    },
    showQuiz() {
      this.quiz = true
    },
  },
}
</script>
