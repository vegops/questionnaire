<template>
  <div id="root">
    <header-component></header-component>
    <main>
      <title-component></title-component>
      <form action="#">
        <questions></questions>
        <input type="submit" value="סיימתי!">
      </form>
    </main>
    <footer-component></footer-component>
  </div>
</template>

<script>
import Header from './Header.vue';
import Title from './Title.vue';
import questions from './questions/questions.vue';
import Footer from './Footer.vue';

export default {
  name: 'Main',
  components: {
    'header-component': Header,
    'title-component': Title,
    'questions': questions,
    'footer-component': Footer
  }
};
</script>
