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
  </div>
</template>

<script>
import Vue from 'vue'

export default {
  data() {
    return {
      result: false,
      quiz: false,
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
