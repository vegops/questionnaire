<template>
  <div class="questions-container">
    <h2 class="questions-h2">
      נסו לענות בשקיפות, כנות ופתיחות :-)
    </h2>
    <div class="questions">
      <ol><question v-for="question in questions" :question="question"></question></ol>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import VueResource from 'vue-resource';
Vue.use(VueResource);
import question from './question.vue';

export default {
  name: 'questions',
  data() {
    return {
      questions: []
    };
  },
  created() {
    return this.$http
      .get('app/questions/questions.json')
      .then(response => response.json())
      .then(response => {
        this.questions = response;
      });
  },
  components: {
    question
  }
};
</script>
