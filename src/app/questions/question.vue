<template>
  <li>
    <div class="question">
      <!-- <img class="question-logo" v-bind:src="questions.logo"/> -->
      <h3 class="question-h3">
        {{ question.question }}
      </h3>
      <div class="answers">
        <input type="radio" class="answer" :name="question.id" value="0"><span>0</span>
        <input type="radio" class="answer" :name="question.id" value="1"><span>1</span>
        <input type="radio" class="answer" :name="question.id" value="2"><span>2</span>
        <input type="radio" class="answer" :name="question.id" value="3"><span>3</span>
        <input type="radio" class="answer" :name="question.id" value="4"><span>4</span>
        <span type="hidden" class="final" :name="question.id"></span>
      </div>
    </div>
  </li>
</template>

<script>

export default {
  name: 'question',
  props: ['question']
};
</script>
