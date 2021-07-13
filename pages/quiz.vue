<template>
  <div>
    <div class="quiz">
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
          <div
            :class="[{ 'd-none': !item.img_a }, 'image']"
            :style="{ backgroundImage: `url('${item.img_a}')` }"
          ></div>
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
          <div
            :class="[{ 'd-none': !item.img_b }, 'image']"
            :style="{ backgroundImage: `url('${item.img_b}')` }"
          ></div>
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
            <template v-if="success">
              <h5>YES, YOU ARE</h5>
              <h2>HYPER FOUNDER!</h2>
              <img src="/choice1.jpg" alt="" />
            </template>
            <template v-else>
              <h5>You were supposed to be</h5>
              <h2>the HYPER one!</h2>
              <img src="/choice2.jpg" alt="" />
            </template>
            <div class="clearfix"></div>
            <a class="link-retake" @click="resetTest()">RETAKE THE TEST</a>
            <div class="clearfix"></div>
            <nuxt-link to="/programs" class="btn btn-primary btn-more">
              <span>See what KOLABORASI can do for you</span>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'

export default {
  data() {
    return {
      result: false,
      quiz: false,
      success: false,
      answer: [],
      hiddenQestion: [],
      question: [
        {
          id: 1,
          quiz: 'How much risk do you take in life?',
          answer_a: 'I tend to play it safe',
          answer_b: 'I eat risk for breakfast',
          img_a: '',
          img_b: '',
        },
        {
          id: 2,
          quiz: 'How do you cope with changes?',
          answer_a: 'I expect them',
          answer_b: 'Lie down, try not to cry, cry a lot',
          img_a: '',
          img_b: '/down.jpeg',
        },
        {
          id: 3,
          quiz: 'Do people look up to you?',
          answer_a: 'Generally, yes',
          answer_b:
            'If I am on the second floor balcony and they’re on the street',
          img_a: '',
          img_b: '',
        },
        {
          id: 4,
          quiz: 'How do you find business opportunities?',
          answer_a: 'Networking events, News, Brainstorming',
          answer_b: 'I wait for it to knock on my doors',
          img_a: '',
          img_b: '',
        },
        {
          id: 5,
          quiz: 'After 6 months, your startup only gained 2 users. What will you do?',
          answer_a: 'Pivot',
          answer_b: 'Pesugihan (Indonesian Witchcraft)',
          img_a: '/pivot.jpg',
          img_b: '/babi.jpg',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Quiz',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
        { hid: 'og:title', name: 'og:title', content: 'Kolaborasi.co | Quiz' },
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
  methods: {
    pickQuiz(index, value) {
      Vue.set(this.answer, index, value)
      setTimeout(() => {
        Vue.set(this.hiddenQestion, index, 'hide')
        if (this.hiddenQestion[this.question.length - 1] === 'hide') {
          let counter = 0
          for (let i = 0; i < this.question.length; i++) {
            if (this.answer[i] === 'a') counter = counter + 1
          }
          if (counter >= 3) this.success = true
          this.result = true
        }
      }, 1000)
    },
    resetTest() {
      this.answer = []
      this.hiddenQestion = []
      this.result = false
      this.success = false
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
